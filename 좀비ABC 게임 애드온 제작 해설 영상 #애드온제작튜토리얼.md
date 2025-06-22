---
title: "좀비ABC 게임 애드온 제작 해설 영상 #애드온제작튜토리얼"
date: "2024-08-23"
thumbnail: "https://i.ytimg.com/vi/Sqs_bcdQC4A/hqdefault.jpg"
tags: ["고급", "베드락", "에듀케이션", "마크1교시", "교과", "애드온제작", "애드온", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=Sqs_bcdQC4A"
duration: "약 9:15"
difficulty: "고급"
---

# 좀비ABC 게임 애드온 제작 해설 영상 #애드온제작튜토리얼

<div align="center">
<img src="https://i.ytimg.com/vi/Sqs_bcdQC4A/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [게임 개요](#게임-개요)
- [애드온 구조](#애드온-구조)
- [핵심 시스템](#핵심-시스템)
- [구현 상세](#구현-상세)
- [커스터마이징](#커스터마이징)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개

이 영상은 좀비ABC 게임 애드온의 제작 과정을 상세히 해설하는 고급 튜토리얼입니다. 베드락 에디션과 교육용 에디션에서 모두 작동하는 완성도 높은 애드온을 만드는 방법을 단계별로 설명합니다.

## 게임 개요

### 1. 좀비ABC 게임이란?
- 좀비를 처치하면 알파벳 블록을 획득하는 게임
- 제한 시간 내에 최대한 많은 단어를 조합하는 것이 목표
- 교육적 요소와 액션을 결합한 창의적 게임

### 2. 기본 규칙
- **좀비 처치**: 좀비를 죽이면 랜덤 알파벳 블록 드롭
- **단어 조합**: 얻은 알파벳 블록으로 단어 만들기
- **시간 제한**: 정해진 시간 내에 게임 진행
- **점수 시스템**: 만든 단어에 따라 점수 획득

## 애드온 구조

### 1. 주요 파일 구성
- **Behavior Pack**: 게임 로직과 시스템
- **Resource Pack**: 텍스처와 모델
- **Functions**: 명령어 모음집
- **Loot Tables**: 아이템 드롭 시스템

### 2. 핵심 컴포넌트
- 스폰 시스템
- 타이머 시스템  
- 스코어보드 관리
- 아이템 드롭 관리

## 핵심 시스템

### 1. 타이머 시스템
```
타이머_s (초 단위): 20틱마다 1씩 증가
타이머_m (분 단위): 타이머_s가 60이 되면 1씩 증가
```

**작동 원리:**
- tick.json에서 1틱마다 실행
- 20틱 = 1초 계산으로 정확한 시간 측정
- 게임 시작/종료 관리

### 2. 좀비 스폰 시스템
```
스폰_타이머: 10초마다 좀비 소환
최대_좀비_수: 15마리 제한
스폰_조건: 특정 구역 내에서만 스폰
```

**구현 방법:**
- function 파일로 스폰 로직 구현
- 스코어보드로 좀비 개수 관리
- 조건부 스폰으로 밸런스 조정

### 3. 알파벳 드롭 시스템
```json
// loot_tables/entities/abc_zombie.json
{
  "pools": [
    {
      "rolls": 1,
      "entries": [
        {
          "type": "item",
          "name": "custom:alphabet_a",
          "weight": 3.8
        },
        // ... 다른 알파벳들
      ]
    }
  ]
}
```

**특징:**
- 각 알파벳 블록이 동일한 확률 (약 3.8%)
- 추가 아이템도 30% 확률로 드롭
- 커스터마이즈 가능한 드롭률

## 구현 상세

### 1. 게임 초기화 (Start Function)
```mcfunction
# function start.mcfunction
scoreboard objectives add timer_s dummy
scoreboard objectives add timer_m dummy
scoreboard objectives add spawn_timer dummy

tag @a[r=50] add spawner
tag @a[r=50] add time_checker
gamemode survival @a
clear @a
```

**실행 과정:**
1. 스코어보드 생성
2. 플레이어에게 태그 부여
3. 게임모드를 서바이벌로 변경
4. 모든 아이템 제거
5. 기본 아이템 지급

### 2. 틱 시스템 (tick.json)
```json
{
  "values": [
    "abc:time_check",
    "abc:spawn_check", 
    "abc:zombie_count"
  ]
}
```

**각 함수 역할:**
- `time_check`: 시간 관리 및 표시
- `spawn_check`: 좀비 스폰 관리  
- `zombie_count`: 좀비 개수 카운트

### 3. 시간 확인 시스템
```mcfunction
# 1초마다 실행 (20틱)
scoreboard players add @a[tag=time_checker] timer_s 1

# 1분 체크
execute @a[scores={timer_s=60}] ~~~ function abc:minute_passed
execute @a[scores={timer_s=60}] ~~~ scoreboard players set @s timer_s 0

# 시간 표시
execute @a[tag=time_checker] ~~~ title @s actionbar 시간: §6§l%timer_m%§r분 §6§l%timer_s%§r초
```

### 4. 좀비 스폰 관리
```mcfunction
# 10초마다 스폰 체크
scoreboard players add @a[tag=spawner] spawn_timer 1

# 좀비 개수가 15마리 미만일 때만 스폰
execute @a[scores={spawn_timer=200}, tag=spawner] ~~~ execute @e[type=zombie, c=15] ~~~ function abc:spawn_zombie

# 스폰 타이머 리셋
scoreboard players set @a[scores={spawn_timer=200}] spawn_timer 0
```

### 5. 게임 종료 처리
```mcfunction
# 10분 경과 시 게임 종료
execute @a[scores={timer_m=10}] ~~~ function abc:stop

# Stop 함수 내용
title @a title §c§l게임 종료!
scoreboard players reset * timer_s
scoreboard players reset * timer_m
tag @a remove spawner
tag @a remove time_checker
```

## 커스터마이징

### 1. 난이도 조정
**쉽게 만들기:**
- 좀비 최대 개수 줄이기 (15 → 10)
- 스폰 주기 늘리기 (10초 → 15초)
- 추가 아이템 드롭률 증가

**어렵게 만들기:**
- 좀비 최대 개수 늘리기
- 스폰 주기 줄이기
- 게임 시간 단축

### 2. 아이템 추가
```json
// 루트 테이블에 새 아이템 추가
{
  "type": "item",
  "name": "minecraft:bread",
  "weight": 5
}
```

### 3. 맵 설정
- 구역 크기 조정 (허용 블록 범위)
- 스폰 구역 변경
- 리스폰 지점 설정

## 자주 묻는 질문

**Q: 베드락 에디션과 교육용 에디션 모두에서 작동하나요?**
A: 네, 이 애드온은 두 에디션 모두에서 완벽하게 작동합니다.

**Q: 난이도를 어떻게 조절하나요?**
A: 좀비 최대 개수, 스폰 주기, 게임 시간 등을 함수 파일에서 수정할 수 있습니다.

**Q: 멀티플레이어에서도 작동하나요?**
A: 네, 여러 플레이어가 경쟁하거나 협력할 수 있도록 설계되었습니다.

**Q: 알파벳 블록의 드롭률을 변경할 수 있나요?**
A: 루트 테이블에서 각 블록의 weight 값을 조정하여 드롭률을 변경할 수 있습니다.

**Q: 게임 시간을 변경하려면?**
A: stop 함수의 조건을 수정하거나 time_check 함수에서 시간 제한을 조정할 수 있습니다.

## 추가 리소스

- [게임 플레이 영상](https://youtu.be/mqpQxrRCUsw)
- [애드온 다운로드 링크](링크)
- [루트 테이블 튜토리얼](링크)
- [베드락 애드온 제작 가이드](링크)

## 이런 분들에게 추천합니다

- 애드온 제작을 배우고 싶은 고급 사용자
- 교육용 게임을 만들고 싶은 교육자
- 베드락 에디션의 고급 기능을 활용하고 싶은 개발자
- 영어 교육과 게임을 결합하고 싶은 교사
- 복잡한 시스템이 있는 미니게임에 관심 있는 제작자

## 기술적 상세

### 스코어보드 시스템
```mcfunction
# 스코어보드 생성
scoreboard objectives add timer_s dummy "초"
scoreboard objectives add timer_m dummy "분"  
scoreboard objectives add spawn_timer dummy "스폰타이머"
scoreboard objectives add zombie_count dummy "좀비수"
```

### 태그 시스템
- **spawner**: 좀비 스폰 권한
- **time_checker**: 시간 체크 권한
- 특정 범위 내 플레이어에게만 부여

### 조건부 실행
```mcfunction
# 좀비가 15마리 미만일 때만 스폰
execute @a[scores={spawn_timer=200}] ~~~ execute @e[type=zombie,c=15] ~~~ say "좀비가 너무 많습니다"
execute @a[scores={spawn_timer=200}] ~~~ execute @e[type=zombie,c=!15] ~~~ function abc:spawn_zombie
```

## 확장 아이디어

### 1. 단어 검증 시스템
- 플레이어가 만든 단어의 유효성 검사
- 점수 시스템 추가
- 단어 데이터베이스 연동

### 2. 특수 좀비 추가
- 보스 좀비: 희귀 알파벳 드롭
- 스피드 좀비: 빠르게 움직임  
- 탱크 좀비: 높은 체력

### 3. 파워업 시스템
- 시간 연장 아이템
- 좀비 처치 버프
- 특수 무기 제공

## 관련 튜토리얼

- [애드온 제작 기초]
- [루트 테이블 심화]
- [함수 시스템 활용]
- [스코어보드 마스터하기]

## 태그
#마인크래프트 #애드온제작 #좀비ABC #베드락 #에듀케이션 #영어교육 #게임개발 #고급 #튜토리얼 #스티브코딩