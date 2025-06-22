---
title: "스코어보드xNPC를 활용한 투표 시스템 구현하기! #NPC커맨드"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/tLpbB9SXfsI/hqdefault.jpg"
tags: ["중급", "에듀케이션", "명령어", "코딩", "월드", "소스코드", "수업자", "롱폼"]
url: "https://www.youtube.com/watch?v=tLpbB9SXfsI"
duration: "7:16"
series: "마인크래프트 명령어 활용"
episode: 
difficulty: "중급"
---

# 스코어보드xNPC를 활용한 투표 시스템 구현하기! #NPC커맨드

<div align="center">
<img src="https://i.ytimg.com/vi/tLpbB9SXfsI/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [시스템 구성 요소](#시스템-구성-요소)
- [구현 과정](#구현-과정)
- [코드 분석](#코드-분석)
- [활용 아이디어](#활용-아이디어)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트에서 스코어보드와 NPC를 결합하여 깔끔한 투표 시스템을 구현하는 방법을 설명합니다. 태그 시스템과 스코어보드를 활용하여 후보자를 등록하고, NPC를 통해 투표를 진행하며, 결과를 실시간으로 확인할 수 있는 기능을 구현합니다. 이 시스템은 교실 내 선거 활동, 게임 내 투표 시스템, 혹은 그룹 의사 결정 도구로 활용될 수 있습니다.

## 시스템 구성 요소

### 1. 태그 시스템
- 플레이어에게 숫자 태그 부여 (1, 2, 3, ...)
- 태그를 통해 후보자 식별

### 2. 스코어보드 
- 세 가지 스코어보드 목표 활용:
  - `번호`: 후보자의 번호 식별
  - `투표`: 플레이어의 투표권 관리
  - `결과`: 각 후보자의 득표수 저장

### 3. NPC 설정
- 투표 NPC 설치
- 각 후보자 번호별 투표 명령 설정
- 투표권 관리 및 결과 반영 기능

## 구현 과정

### 1. 후보자 등록 (00:10-01:30)
- 커맨드 블록을 사용하여 플레이어에게 태그 부여
- 레드스톤 신호로 커맨드 블록 활성화
- 각 후보자에게 1, 2, 3 등의 태그 할당

### 2. 스코어보드 설정 (01:30-03:10)
- 스코어보드 목표 생성: 번호, 투표, 결과
- 모든 플레이어에게 투표권 1개 부여
- 태그를 기반으로 후보자 번호 설정

### 3. NPC 투표 시스템 (03:10-05:30)
- NPC 설치 및 대화 옵션 구성
- 후보자 번호 선택 시 투표 실행
- 투표 완료 후 투표권 차감

### 4. 결과 확인 및 초기화 (05:30-끝)
- 투표 결과 사이드바에 표시
- 투표권 초기화 기능
- 투표 결과 초기화 기능

## 코드 분석

### 후보자 태그 부여
```
/tag @p[distance=..2] add 1
/tag @p[distance=..2] add 2
/tag @p[distance=..2] add 3
```
- `@p[distance=..2]`: 명령어 실행 지점으로부터 2블록 이내의 가장 가까운 플레이어
- `add 1`: 태그 '1' 추가

### 스코어보드 초기 설정
```
/scoreboard objectives add 번호 dummy
/scoreboard objectives add 투표 dummy
/scoreboard objectives add 결과 dummy
/scoreboard players set @a 투표 1
/scoreboard players set @a 결과 0
/scoreboard players set @a[tag=1] 번호 1
/scoreboard players set @a[tag=2] 번호 2
/scoreboard players set @a[tag=3] 번호 3
```

### 투표 표시 명령어
```
/scoreboard objectives setdisplay sidebar 투표
```

### 결과 표시 명령어
```
/scoreboard objectives setdisplay sidebar 결과
```

### NPC 투표 명령어 (1번 후보 예시)
```
/scoreboard players add @a[tag=1] 결과 1
/scoreboard players remove @p 투표 1
```
- 태그가 '1'인 플레이어(1번 후보)의 결과 값 1 증가
- 투표를 실행한 플레이어의 투표권 1 감소

### 투표권 초기화
```
/scoreboard players set @a 투표 1
```

### 결과 초기화
```
/scoreboard players set @a 결과 0
```

## 활용 아이디어

### 교육 환경
1. **학급 임원 선거**: 실제 학급 선거 과정을 게임으로 재현
2. **의견 수렴**: 학습 주제나 활동 선택에 대한 학생들의 의견 수집
3. **토론 활동**: 찬반 토론 후 투표를 통한 승패 결정

### 게임 활용
1. **게임 룰 설정**: 다음 게임 모드나 규칙 선택
2. **역할 분담**: 팀 플레이에서 각 역할 배정
3. **건축 콘테스트**: 여러 건축물 중 가장 좋은 작품 선정

### 확장 기능
1. **다중 투표**: 여러 개의 투표권 부여
2. **가중치 투표**: 특정 조건에 따라 투표 가중치 부여
3. **익명 투표**: 투표자 정보 숨기기
4. **투표 마감 시간**: 타이머 설정을 통한 자동 마감

## 자주 묻는 질문

**Q: 한 플레이어가 여러 번 투표할 수 있나요?**
A: 기본 설정에서는 모든 플레이어에게 1개의 투표권만 주어지므로 한 번만 투표할 수 있습니다. 만약 여러 번 투표를 허용하고 싶다면 투표권 수를 조정하면 됩니다.

**Q: 최대 몇 명의 후보를 등록할 수 있나요?**
A: 영상에서는 3명의 후보만 보여주었지만, 원하는 만큼 확장할 수 있습니다. 영상에서 언급했듯이 NPC에는 최대 30명까지의 후보 옵션을 미리 설정해둘 수 있습니다.

**Q: 투표 결과가 동점일 경우 어떻게 처리하나요?**
A: 기본 시스템에서는 동점 처리에 대한 특별한 기능은 없습니다. 필요하다면 추가 코드를 작성하여 동점자 간 결선 투표 등의 기능을 구현할 수 있습니다.

**Q: 이 시스템을 멀티플레이어 서버에서 사용할 수 있나요?**
A: 네, 멀티플레이어 환경에서도 잘 작동합니다. 다만, 태그 부여 시 여러 플레이어가 커맨드 블록 근처에 있으면 의도치 않은 대상에게 태그가 부여될 수 있으니 주의해야 합니다.

**Q: 투표를 완료한 플레이어와 하지 않은 플레이어를 구분할 수 있나요?**
A: 네, 투표권 스코어보드 값을 통해 구분할 수 있습니다. 투표를 완료한 플레이어는 투표권이 0이 되고, 아직 투표하지 않은 플레이어는 1이 남아있습니다.

## 추가 리소스
- [전체 명령어 코드 확인 링크](https://stevecoding.kr/commands/)
- [스티브코딩 유튜브 채널](https://www.youtube.com/c/stevecoding)
- [마인크래프트 명령어 공식 위키](https://minecraft.fandom.com/wiki/Commands)
- [NPC 관련 추가 튜토리얼 영상](https://youtube.com/link-to-related-video)
- [스코어보드 활용 게임 제작 가이드](https://link-to-guide)

## 이런 분들에게 추천합니다
- 마인크래프트를 교육 도구로 활용하는 교사
- 게임 내 미니게임이나 이벤트를 운영하는 서버 관리자
- 투표 시스템이 필요한 팀 프로젝트 참여자
- 마인크래프트 명령어와 NPC 기능에 관심 있는 플레이어
- 게임을 통한 민주적 의사결정 과정을 경험하고 싶은 교육자

## 관련 튜토리얼
- [스코어보드 돈 벌기 시스템 구현하기! #코드작성기활용](https://www.youtube.com/watch?v=관련영상링크)
- [스코어보드와 NPC로 상인 만들기! (반복 작업 없이 쉽게!)](https://www.youtube.com/watch?v=관련영상링크)
- [돈을 많이 가지고 있으면 더 비싸게 받는 NPC 상인](https://www.youtube.com/watch?v=관련영상링크)
- [커맨드블록 + NPC = 완벽한 상인! #마인크래프트가이드](https://www.youtube.com/watch?v=관련영상링크)

## 전체 명령어 코드

### 태그 부여용 커맨드 블록
```
/tag @p[distance=..2] add 1
/tag @p[distance=..2] add 2
/tag @p[distance=..2] add 3
```

### 스코어보드 초기 설정 (채팅 명령어 "1")
```
/scoreboard objectives add 번호 dummy
/scoreboard objectives add 투표 dummy
/scoreboard objectives add 결과 dummy
/scoreboard players set @a 투표 1
/scoreboard players set @a 결과 0
/scoreboard players set @a[tag=1] 번호 1
/scoreboard players set @a[tag=2] 번호 2
/scoreboard players set @a[tag=3] 번호 3
```

### 투표권 표시 (채팅 명령어 "v")
```
/scoreboard objectives setdisplay sidebar 투표
```

### 결과 표시 (채팅 명령어 "r")
```
/say 투표 결과를 보여줍니다
/scoreboard objectives setdisplay sidebar 결과
```

### 투표권 초기화 (채팅 명령어 "c")
```
/scoreboard players set @a 투표 1
```

### 결과 초기화 (채팅 명령어 "clear")
```
/scoreboard players set @a 결과 0
```

### NPC 투표 명령 (1번 후보 예시)
```
/scoreboard players add @a[tag=1] 결과 1
/scoreboard players remove @p 투표 1
```

## 태그
#마인크래프트 #스코어보드 #NPC #투표시스템 #명령어 #코드작성기 #에듀케이션에디션 #교육용게임 #게임기반학습 #스티브코딩
