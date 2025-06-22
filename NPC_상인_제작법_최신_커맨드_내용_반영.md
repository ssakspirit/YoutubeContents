---
title: "NPC 상인 제작법 (최신 커맨드 내용 반영)"
date: "2025-04-26"
thumbnail: "https://i.ytimg.com/vi/1W3wTc8Vhhc/hqdefault.jpg"
tags: ["중급", "베드락", "에듀케이션", "명령어", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=1W3wTc8Vhhc"
duration: "2:27"
series: "마인크래프트 커맨드 튜토리얼"
episode: 1
difficulty: "중급"
---

# NPC 상인 제작법 (최신 커맨드 내용 반영)

<div align="center">
<img src="https://i.ytimg.com/vi/1W3wTc8Vhhc/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션과 에듀케이션 에디션에서 물물교환 형태의 NPC 상인을 만드는 방법을 설명합니다. 최신 커맨드 구문을 활용하여, 플레이어가 특정 아이템을 가지고 있을 때만 거래가 가능하도록 설정하는 기능을 구현합니다. 이 튜토리얼에서는 썩은 고기 10개를 다이아몬드 1개로 교환하는 상인을 예시로 보여줍니다.

## 주요 내용
### 1. NPC 상인 작동 원리
- 물물교환 시스템의 기본 구조
- 플레이어 인벤토리 확인 메커니즘
- 아이템 제거 및 지급 로직

### 2. 핵심 커맨드 소개
- execute 명령어와 as/at 구문 활용법
- hasitem 선택자를 통한 아이템 확인
- 조건부 명령어 실행 방법
- clear와 give 명령어 활용

### 3. 메시지 피드백 시스템
- 아이템 부족 시 안내 메시지 표시
- 거래 성공 시 확인 메시지 제공
- 커맨드 블록 연결 방식 이해

## 실습 과정
1. **NPC 상인 동작 확인 (00:00-00:35)**
   - "지킴이 선생님" NPC와의 상호작용 시연
   - 썩은 고기 10개를 다이아몬드 1개로 교환 과정
   - 아이템 부족 시 표시되는 메시지 확인

2. **커맨드 구성 분석 (00:36-01:25)**
   - 커맨드 블록 구조 및 연결 방식 설명
   - 4개의 명령어 순차적 실행 방식
   - 첫 번째와 두 번째 명령어: 메시지 표시 로직

3. **아이템 교환 명령어 (01:26-02:27)**
   - 세 번째 명령어: 다이아몬드 지급 메커니즘
   - 네 번째 명령어: 썩은 고기 제거 방법
   - hasitem 선택자와 quantity 옵션 상세 설명
   - 데이터 값과 아이템 개수 설정 방법

## 자주 묻는 질문
**Q: 이 시스템은 여러 종류의 아이템을 동시에 거래할 수 있나요?**
A: 기본 구조를 확장하여 여러 종류의 아이템을 거래할 수 있습니다. 각 거래 유형별로 별도의 커맨드 블록 세트를 설정하고, NPC의 대화에 여러 버튼을 추가하면 다양한 거래 옵션을 제공할 수 있습니다.

**Q: 플레이어가 아이템을 충분히 가지고 있는지 확인하는 다른 방법이 있나요?**
A: 네, testfor 명령어나 scoreboard 시스템을 활용할 수도 있지만, 이 영상에서 소개한 hasitem 선택자가 가장 직관적이고 효율적인 방법입니다.

**Q: 거래 횟수에 제한을 둘 수 있나요?**
A: 스코어보드 명령어를 추가하여 플레이어별 거래 횟수를 추적하고, 일정 횟수 이상 거래가 불가능하도록 설정할 수 있습니다.

## 추가 리소스
- [마인크래프트 베드락 에디션 커맨드 공식 문서](https://minecraft.gamepedia.com/Commands/Bedrock_Edition)
- [마인크래프트 에듀케이션 NPC 가이드](https://education.minecraft.net/ko-kr/resources/computer-science-subject-kit)
- [execute 명령어 심화 활용 가이드](링크)
- [스티브코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)

## 이런 분들에게 추천합니다
- 마인크래프트에서 커스텀 상점 시스템을 구현하고 싶은 맵 제작자
- 교육용 서버에서 보상 시스템을 개발하려는 교사
- 최신 커맨드 구문을 배우고 싶은 마인크래프트 유저
- 학생들에게 게임 내 경제 시스템을 가르치고 싶은 교육자

## 관련 튜토리얼
- [커맨드블록 + NPC = 완벽한 상인! #마인크래프트가이드](https://www.youtube.com/watch?v=...)
- [NPC를 상인으로 만들어보자! #마인크래프트가이드](https://www.youtube.com/watch?v=...)
- [스코어보드와 NPC로 상인 만들기! (반복 작업 없이 쉽게!)](https://www.youtube.com/watch?v=...)

## 실습 코드
```
# NPC 상인 제작을 위한 명령어 (썩은 고기 10개 → 다이아몬드 1개 교환)

# 1. 아이템 부족 시 메시지 출력
/execute as @initiator[hasitem={item=rotten_flesh, quantity=..9}] at @s run say 썩은 고기가 부족하다...

# 2. 거래 성공 메시지 출력
/execute as @initiator[hasitem={item=rotten_flesh, quantity=10..}] at @s run say 썩은 고기 10개를 다이아 한 개로 바꿨었다!

# 3. 다이아몬드 지급
/execute as @initiator[hasitem={item=rotten_flesh, quantity=10..}] at @s run give @s diamond

# 4. 썩은 고기 제거
/execute as @initiator[hasitem={item=rotten_flesh, quantity=10..}] at @s run clear @s rotten_flesh 0 10
```

## 태그
`#마인크래프트` `#NPC상인` `#커맨드블록` `#execute명령어` `#hasitem` `#물물교환` `#게임경제` `#교육용마인크래프트`