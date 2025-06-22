---
title: "커맨드 2개로 되는 완전 간편한 NPC상점(hasitem활용)"
date: "2022-04-23"
thumbnail: "https://i.ytimg.com/vi/y-8iMUrBpcY/hqdefault.jpg"
tags: ["중급", "베드락", "에듀케이션", "명령어", "설계자", "애드온", "롱폼"]
url: "https://www.youtube.com/watch?v=y-8iMUrBpcY"
duration: "3:50"
series: "마인크래프트 코딩 튜토리얼"
difficulty: "중급"
---

# 커맨드 2개로 되는 완전 간편한 NPC상점(hasitem활용)

<div align="center">
<img src="https://i.ytimg.com/vi/y-8iMUrBpcY/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 에듀케이션 에디션 1.18.3 업데이트에서 추가된 `hasitem` 대상 선택 인자를 활용하여 매우 간단하게 NPC 상점을 만드는 방법을 설명합니다. `hasitem` 인자를 사용하면 이전보다 훨씬 쉽게 아이템 거래 시스템을 구현할 수 있습니다.

## 주요 내용

### 1. hasitem 인자 활용하기
- 플레이어가 특정 아이템을 가지고 있는지 확인하는 방법
- 아이템의 종류와 수량을 조건으로 설정하는 방법
- @initiator 선택자를 통한 NPC 상호작용 감지

### 2. NPC 상점 시스템 구축
- 간단한 두 가지 거래 기능 만들기 (에메랄드 2개 → 황금사과 1개, 에메랄드 1개 → 사과 1개)
- execute와 clear 명령어를 조합한 거래 시스템
- 하나의 NPC로 여러 거래 옵션 제공하기

### 3. hasitem 인자 세부 설정
- 아이템 이름(item) 지정하기
- 데이터 값(data) 설정하기
- 아이템 위치(location) 지정하기
- 슬롯(slot) 번호 활용하기
- 수량(quantity) 조건 설정하기

## 실습 과정

1. **NPC 상점 설계 및 구현 (00:00-01:30)**
   - 에메랄드 블록을 화폐로 사용하는 상점 시스템 소개
   - NPC를 통한 아이템 거래 시연 (에메랄드 2개로 황금사과 구매, 에메랄드 1개로 일반 사과 구매)
   - 거래 완료 시 자동으로 에메랄드 차감 및 아이템 지급 확인

2. **NPC 코드 분석 (01:31-03:00)**
   - execute @initiator 명령어 설명
   - hasitem 대상 선택 인자 구문 분석
   - give와 clear 명령어 조합을 통한 거래 메커니즘 설명
   - 수량 조건 설정 (quantity=2..)의 의미 해석

3. **hasitem 인자 심화 활용 (03:01-끝)**
   - item 파라미터: 아이템 이름 지정
   - data 파라미터: 아이템 데이터 값 설정
   - location 파라미터: 아이템 위치 확인 (인벤토리, 상자 등)
   - slot 파라미터: 특정 슬롯에 있는 아이템 확인 (0부터 시작하는 슬롯 번호 설명)
   - 다양한 조건 조합을 통한 복잡한 거래 시스템 구현 가능성 소개

## 자주 묻는 질문

**Q: hasitem 인자는 어떤 버전부터 사용할 수 있나요?**  
A: 이 기능은 마인크래프트 에듀케이션 에디션 1.18.3 업데이트부터 정식으로 추가되었습니다. 베드락 에디션에서도 동일한 버전 이상에서 사용 가능합니다.

**Q: 한 NPC에 여러 가지 거래를 추가할 수 있나요?**  
A: 네, 영상에서 보여주는 것처럼 하나의 NPC에 여러 개의 명령어를 추가하여 다양한 거래 옵션을 제공할 수 있습니다.

**Q: 특정 슬롯에 있는 아이템만 확인하려면 어떻게 해야 하나요?**  
A: hasitem 인자에서 slot 파라미터를 추가하여 특정 슬롯에 있는 아이템만 확인할 수 있습니다. slot 번호는 0부터 시작합니다.

**Q: 다른 종류의 아이템으로도 거래할 수 있나요?**  
A: 네, hasitem 인자에서 item 파라미터를 변경하여 어떤 아이템이든 거래 화폐로 사용할 수 있습니다.

## 추가 리소스
- [마인크래프트 공식 위키 - 명령어](https://minecraft.fandom.com/wiki/Commands)
- [마인크래프트 에듀케이션 에디션 공식 사이트](https://education.minecraft.net/)
- [스티브 코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)

## 이런 분들에게 추천합니다
- 마인크래프트 에듀케이션 에디션에서 간단한 상점 시스템을 구현하고 싶은 교사와 학생
- 명령어를 활용하여 게임 메커니즘을 구현하고 싶은 중급 이상의 사용자
- NPC와 상호작용하는 맵이나 게임을 만들고 싶은 제작자
- 마인크래프트에서 경제 시스템을 구현하고 싶은 서버 운영자

## 관련 튜토리얼
- 커맨드블록 + NPC = 완벽한 상인! #마인크래프트가이드
- 플레이어를 우클릭하면 UI창이 뜸!
- 퀴즈 NPC에서 보상을 중복으로 받지 못하게 하기

## 실습 코드
```
# 에메랄드 블록2개 주고 황금사과 1개얻기
/execute @initiator[hasitem={item=emerald, quantity=2..}] ~~~ give @s golden_apple
/clear @initiator[hasitem={item=emerald, quantity=2..}] emerald 0 2

# 에메랄드 블록1개 주고 사과 1개얻기
/execute @initiator[hasitem={item=emerald, quantity=1..}] ~~~ give @s apple
/clear @initiator[hasitem={item=emerald, quantity=1..}] emerald 0 1
```

## 태그
#마인크래프트 #커맨드 #NPC #상점 #hasitem #에듀케이션에디션 #베드락 #스티브코딩 #명령어