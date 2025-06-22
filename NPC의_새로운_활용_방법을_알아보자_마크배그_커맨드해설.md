---
title: "NPC의 새로운 활용 방법을 알아보자! 마크배그 커맨드해설"
date: "2025-04-26"
thumbnail: "https://i.ytimg.com/vi/Y-wxASo6mXM/hqdefault.jpg"
tags: ["고급", "베드락", "에듀케이션", "애드온제작", "명령어", "게임", "월드", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=Y-wxASo6mXM"
duration: "7:42"
series: "커맨드 해설 시리즈"
episode: 1
difficulty: "고급"
---

# NPC의 새로운 활용 방법을 알아보자! 마크배그 커맨드해설

<div align="center">
<img src="https://i.ytimg.com/vi/Y-wxASo6mXM/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션과 에듀케이션 에디션에서 NPC를 활용한 고급 게임 구현 방법을 소개합니다. '마크배그(마인크래프트 배틀그라운드)'라는 게임을 구현한 커맨드 시스템을 자세히 해설하며, NPC가 아이템을 주거나 무작위로 이동하는 방식, 게임 시작과 종료 시스템, 플레이어 사망 처리 등 복잡한 게임 메커니즘이 어떻게 구현되었는지 상세히 설명합니다.

## 주요 내용
### 1. 마크배그 게임 시스템 개요
- 게임 시작 및 종료 기능
- 사이드바 스코어보드를 활용한 점수 시스템
- 타이머와 플레이어 이동 메커니즘
- 죽음 처리 및 리스폰 시스템

### 2. NPC의 고급 활용 기법
- NPC를 통한 특별 아이템 배포
- 무작위 위치로 이동하는 NPC 구현
- spreadplayers 명령어를 활용한 NPC 배치
- 특정 NPC의 고정 위치 유지 방법

### 3. 커맨드 블록 체인 시스템
- 반복 커맨드 블록과 일반 커맨드 블록의 구분
- 레드스톤 블록을 활용한 명령어 체인 구현
- 태그 시스템을 활용한 조건부 명령어 실행
- 효율적인 명령어 체인 디자인 방법

## 실습 과정
1. **게임 시스템 둘러보기 (00:00-01:30)**
   - 게임 시작 및 카운트다운 확인
   - 사이드바 스코어보드 표시 방식
   - NPC를 통한 아이템 획득 과정
   - 플레이어 사망 및 리스폰 시스템 확인

2. **명령어 시스템 해석 (01:31-03:30)**
   - NPC 커맨드 및 고급 설정 살펴보기
   - NPC 이동 메커니즘 (spreadplayers 명령어)
   - 버튼 모드를 사용하지 않는 이유
   - 자동 실행되는 명령어 체인 구조

3. **게임 시작/종료 커맨드 분석 (03:31-05:30)**
   - 스코어보드 초기화 및 아이템 지급 명령어
   - 타이틀 및 안내 메시지 설정 방법
   - 레드스톤 블록 설치 및 제거 메커니즘
   - 인게임 타이머 구현 방식

4. **플레이어 사망 처리 시스템 (05:31-07:42)**
   - 죽은 플레이어 감지 및 태그 부여
   - 스코어보드 값 증가 및 리스폰 처리
   - 효과 부여 및 아이템 재지급 방식
   - 태그 삭제를 통한 명령어 중복 실행 방지

## 자주 묻는 질문
**Q: NPC를 무작위 위치로 이동시키는 spreadplayers 명령어의 구문은 어떻게 되나요?**
A: 기본 구문은 `spreadplayers <x> <z> <spreadDistance> <maxRange> <respectTeams> <target>` 입니다. 영상에서는 `spreadplayers ~ ~ 0 90 false @e[type=npc]`와 같은 형태로 사용되었으며, 이는 현재 위치를 중심으로 90블록 범위 내에 NPC들을 무작위로 배치하는 명령입니다.

**Q: 특정 NPC만 고정 위치에 유지하는 방법은 무엇인가요?**
A: 특정 NPC에 이름을 부여하고(`name=특정이름`), 해당 이름을 가진 NPC만 선택하는 선택자(`@e[type=npc,name=특정이름]`)를 사용하여 tp 명령어로 고정 위치로 텔레포트시키는 방법을 사용합니다.

**Q: 플레이어가 죽었을 때 태그를 사용하는 이유는 무엇인가요?**
A: 태그를 사용하면 특정 조건의 플레이어만 선택적으로 명령어를 실행할 수 있습니다. 죽은 플레이어에게 태그를 부여한 후, 해당 태그를 가진 플레이어에게만 효과 부여, 아이템 지급 등의 명령을 실행하고, 모든 처리가 끝나면 태그를 제거하여 중복 실행을 방지합니다.

## 추가 리소스
- [마크배그 월드 다운로드 링크](링크)
- [스프레드플레이어 명령어 공식 문서](https://minecraft.gamepedia.com/Commands/spreadplayers)
- [NPC 커맨드 상세 가이드](링크)
- [채널 송's 시간 체크 시스템 설명 영상](링크)
- [스티브코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)

## 이런 분들에게 추천합니다
- 고급 커맨드 시스템 구현에 관심 있는 맵 제작자
- NPC를 단순 대화 외에 다양하게 활용하고 싶은 분
- 마인크래프트로 미니게임을 만들고 싶은 서버 운영자
- 코딩 없이 복잡한 게임 메커니즘을 구현하고 싶은 교육자

## 관련 튜토리얼
- [NPC를 상인으로 만들어보자! #마인크래프트가이드](https://www.youtube.com/watch?v=BnPfCoTxaoU)
- [오늘 저녁은 치킨이닭! _ 메이크코드 #66 마크 배틀그라운드](https://www.youtube.com/watch?v=...)
- [NPC 상인 제작법 (최신 커맨드 내용 반영)](https://www.youtube.com/watch?v=1W3wTc8Vhhc)

## 실습 코드
```
# 주요 명령어 모음

# NPC 무작위 이동 명령어
spreadplayers ~ ~ 0 90 false @e[type=npc]

# 메인 NPC 고정 위치 유지
tp @e[type=npc,name=메인] <x> <y> <z>

# 게임 시작 시 스코어보드 및 타이머 설정
scoreboard objectives add 죽음 dummy "아주금"
scoreboard objectives setdisplay sidebar 죽음
scoreboard objectives add 분 dummy
scoreboard objectives add 초 dummy
scoreboard players set @a 분 4
scoreboard players set @a 초 0

# 플레이어 사망 처리
tag @a[x=<x>,y=<y>,z=<z>,r=3] add 죽은사람
effect give @a[tag=죽은사람] regeneration 10 255 true
scoreboard players add @a[tag=죽은사람] 죽음 1
spreadplayers <x> <z> 10 50 false @a[tag=죽은사람]
tag @a[tag=죽은사람] remove 죽은사람
```

## 태그
`#마인크래프트` `#NPC활용` `#커맨드블록` `#마크배그` `#게임제작` `#spreadplayers` `#스코어보드` `#태그시스템` `#고급커맨드`