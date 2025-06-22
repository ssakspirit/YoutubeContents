---
title: "일정 시간마다 보상을 주는 커맨드! function으로 구현하기! #애드온제작튜토리얼"
date: "2025-05-20"
thumbnail: "https://i.ytimg.com/vi/TxNofzb5Zcg/hqdefault.jpg"
tags: ["고급", "베드락", "에듀케이션", "명령어", "애드온제작", "애드온", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=TxNofzb5Zcg"
duration: "7:46"
series: "애드온제작튜토리얼"
episode: ""
difficulty: "고급"
---

# 일정 시간마다 보상을 주는 커맨드! function으로 구현하기! #애드온제작튜토리얼

<div align="center">
  <img src="https://i.ytimg.com/vi/TxNofzb5Zcg/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [Function 기본 개념](#function-기본-개념)
- [골드 타이머 구현](#골드-타이머-구현)
- [tick.json 활용](#tickjson-활용)
- [Function 파일 작성](#function-파일-작성)
- [스코어보드 시스템](#스코어보드-시스템)
- [실시간 반영 방법](#실시간-반영-방법)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개

마인크래프트 베드락 에디션에서 Function을 활용하여 일정 시간마다 자동으로 보상을 지급하는 시스템을 구현하는 방법을 다룹니다. tick.json을 통한 자동 실행부터 스코어보드를 이용한 타이머 구현까지 상세히 설명합니다.

## 주요 내용

### 1. 골드 타이머 애드온 시연 (0:00-1:00)
- 60초마다 자동으로 금괴 지급
- 액션바에 실시간 타이머 표시
- 자동 초기화 및 반복 시스템

### 2. Function 기본 구조 소개 (1:00-2:30)
- tick.json의 역할과 활용법
- Function 파일(.mcfunction) 생성 방법
- 여러 명령어의 순차적 실행

### 3. 실제 구현 과정 (2:30-7:00)
- 스코어보드를 이용한 타이머 시스템
- 조건문을 통한 보상 지급 로직
- Function 간의 연동 방법

## Function 기본 개념

### tick.json이란?
- **위치**: 행동팩 최상위 폴더의 `tick.json`
- **역할**: 매 틱(1/20초)마다 실행할 Function 지정
- **문법**: JSON 형식으로 Function 배열 작성

```json
{
  "values": [
    "gold_timer"
  ]
}
```

### Function 파일 구조
- **확장자**: `.mcfunction`
- **위치**: `functions/` 폴더 내
- **특징**: 
  - 여러 명령어를 순차적으로 실행
  - `#`으로 주석 추가 가능
  - 자동완성 지원

## 골드 타이머 구현

### 1. 프로젝트 설정 (1:15-1:45)
- **이름**: GoldTimer
- **버전**: 1.19+
- **타겟**: 베드락 에디션, 교육용 에디션

### 2. 메인 Function 작성 (1:45-3:30)

**파일**: `functions/gold_timer.mcfunction`

```mcfunction
# 시간 초기화
scoreboard objectives add gold_timer dummy
scoreboard objectives add gold_timer_s dummy

# 골드 타이머 1틱마다 증가
scoreboard players add @a gold_timer 1

# 20틱(1초)마다 초 카운터 증가
execute if score @a gold_timer matches 20.. run scoreboard players add @a gold_timer_s 1
execute if score @a gold_timer matches 20.. run scoreboard players set @a gold_timer 0

# 60초 도달시 보상 지급
execute if score @a gold_timer_s matches 60.. run function pay
execute if score @a gold_timer_s matches 60.. run scoreboard players set @a gold_timer_s 0

# 액션바에 타이머 표시
title @a actionbar "Time: " score @a gold_timer_s "s"
```

### 3. 보상 Function 작성 (3:30-4:00)

**파일**: `functions/pay.mcfunction`

```mcfunction
# 골드 타이머 보상
give @a gold_ingot 1
title @a title "보상 지급!"
```

## 스코어보드 시스템

### 타이머 구조
1. **gold_timer**: 매 틱마다 증가 (0-19 반복)
2. **gold_timer_s**: 매 20틱(1초)마다 증가
3. **조건 검사**: 60초 도달 시 보상 및 초기화

### 시간 계산
- **1틱** = 1/20초 (약 0.05초)
- **20틱** = 1초
- **1200틱** = 60초 (1분)

## tick.json 활용

### 기본 문법 (1:30-2:00)
```json
{
  "values": [
    "function_name1",
    "function_name2"
  ]
}
```

### 자동 실행 원리
- 게임 로딩 시 자동으로 tick.json 읽기
- 매 틱마다 지정된 Function들 순차 실행
- 월드가 실행되는 동안 지속적으로 작동

## Function 파일 작성

### 주석 활용 (2:20-2:50)
```mcfunction
# 이것은 주석입니다
scoreboard objectives add timer dummy # 인라인 주석

# 여러 줄 주석도 가능
# 복잡한 설명이 필요할 때 사용
```

### 명령어 자동완성 (2:50-3:00)
- Function 에디터에서 Ctrl+Space로 자동완성
- 명령어 문법 실시간 검증
- 오타 방지 및 효율적 작성

## 실시간 반영 방법

### reload 명령어 활용 (6:30-7:30)
```
/reload
```

### 주의사항
- **기존 Function 수정**: `/reload`로 즉시 반영
- **새 Function 추가**: 월드 재시작 필요
- **tick.json 수정**: 월드 재시작 필요

### 테스트 방법
```mcfunction
# Function 직접 실행
/function pay

# 스코어보드 확인
/scoreboard players set @s gold_timer_s 59
```

## 고급 활용법

### 조건부 실행 (4:00-5:00)
```mcfunction
# 여러 조건 조합
execute if score @a gold_timer_s matches 60.. if entity @a[tag=premium] run function premium_pay

# 위치 기반 조건
execute if score @a gold_timer_s matches 60.. at @a[x=100,y=64,z=100,r=10] run function area_bonus
```

### 복합 타이머 시스템
```mcfunction
# 시, 분, 초 구현
execute if score @a timer_s matches 60.. run scoreboard players add @a timer_m 1
execute if score @a timer_m matches 60.. run scoreboard players add @a timer_h 1
execute if score @a timer_m matches 60.. run scoreboard players set @a timer_m 0
```

### 다양한 보상 시스템
```mcfunction
# 랜덤 보상
execute if score @a gold_timer_s matches 60.. run function random_reward

# 누적 보상
execute if score @a gold_timer_s matches 60.. run scoreboard players add @a total_gold 1
execute if score @a total_gold matches 10.. run function milestone_reward
```

## 자주 묻는 질문

**Q: tick.json이 작동하지 않아요.**  
A: tick.json 파일이 행동팩 최상위 폴더에 있는지, JSON 문법이 올바른지 확인하세요. 월드를 재시작해야 적용됩니다.

**Q: Function에서 오류가 발생해요.**  
A: Function 파일명과 실제 호출하는 이름이 일치하는지 확인하고, `/reload`를 실행해 보세요.

**Q: 스코어보드가 초기화되지 않아요.**  
A: `scoreboard objectives add` 명령어는 이미 존재하는 목표에 대해서는 오류를 발생시키지 않으므로 안전합니다.

**Q: 여러 명령어를 동시에 실행하고 싶어요.**  
A: Function 파일에 순서대로 작성하면 모두 같은 틱에 순차적으로 실행됩니다.

## 추가 리소스

- [골드타이머 애드온 다운로드](영상 설명란 링크)
- [Function 공식 문서](링크)
- [스코어보드 명령어 가이드](링크)
- [조건부 실행 심화 가이드](링크)

## 이런 분들에게 추천합니다
- 애드온 제작을 처음 시작하는 초보자
- 자동화 시스템 구현에 관심 있는 개발자
- 서버 관리용 도구가 필요한 관리자
- 복잡한 게임 시스템을 만들고 싶은 크리에이터

## 활용 예시
- **로그인 보상**: 접속 시간에 따른 자동 보상
- **이벤트 타이머**: 정해진 시간에 이벤트 실행
- **자동 세이브**: 일정 간격으로 데이터 저장
- **시간 기반 게임**: 실시간으로 변화하는 게임 요소

## 확장 아이디어
- **레벨링 시스템**: 시간에 따른 경험치 획득
- **기지 방어**: 주기적으로 몬스터 스폰
- **자원 생성**: 시간당 자원 자동 생성
- **퀘스트 시스템**: 일일/주간 퀘스트 갱신

## 최적화 팁
- 불필요한 계산 최소화
- 조건문 순서 최적화
- 스코어보드 정리 및 관리
- Function 분할을 통한 모듈화

## 주의사항
- tick.json은 성능에 직접적인 영향
- 과도한 계산은 지연 현상 유발 가능
- 백업을 통한 안전한 개발 권장
- 테스트 환경에서 충분한 검증 필요

## 태그
`#애드온제작` `#Function` `#tick.json` `#스코어보드` `#자동화` `#타이머` `#보상시스템` `#베드락`