---
title: "말이 많은 NPC 만들기! #애드온제작튜토리얼"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/PvXc6XPnYaw/hqdefault.jpg"
tags: ["중급", "에듀케이션", "베드락", "애드온제작", "애드온", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=PvXc6XPnYaw"
duration: "11:36"
series: "애드온 제작 튜토리얼"
episode: 1
difficulty: "중급"
---

# 말이 많은 NPC 만들기! #애드온제작튜토리얼

<div align="center">
<img src="https://i.ytimg.com/vi/PvXc6XPnYaw/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락/에듀케이션 에디션에서 대화형 NPC를 생성하는 방법을 다루는 애드온 제작 튜토리얼입니다. Bridge 프로그램을 활용하여 복잡한 대화 시스템을 구현하는 방법을 소개하며, 여러 대화 시나리오와 선택지, 보상 시스템까지 포함한 상호작용성 높은 NPC를 만드는 과정을 단계별로 설명합니다. 이를 통해 마인크래프트 게임 내 스토리텔링과 퀘스트 시스템을 더욱 풍부하게 구현할 수 있습니다.

## 주요 내용

### 1. NPC 대화 시스템 이해하기
- 다이얼로그(Dialogue) 폴더 구조와 역할 설명
- 대화 장면(Scene)과 NPC 상호작용 원리 이해
- JSON 파일 구조를 통한 대화 시나리오 설계 방법

### 2. Bridge 프로그램을 활용한 다이얼로그 제작
- Bridge 프로그램에서 JSON 파일 편집하기
- 대화 장면 번호(Scene)와 버튼, 명령어 설정 방법
- 코드 자동 완성 및 오류 검사 기능 활용하기

### 3. 다양한 대화 분기와 상호작용 구현
- 대화 시나리오 분기 설계와 장면 전환 방법
- 버튼 클릭에 따른 다양한 반응과 명령어 실행
- NPC가 플레이어에게 아이템을 제공하는 보상 시스템 구현
- 대화의 연속성과 다양한 종료 조건 설정하기

## 실습 과정
1. **애드온 다운로드 및 초기 설정 (00:00-03:00)**
   - 제공된 링크에서 애드온 다운로드하기
   - Bridge 프로그램에서 프로젝트 불러오기
   - 다이얼로그 폴더 구조와 JSON 파일 확인하기

2. **다이얼로그 JSON 파일 분석 (03:01-06:00)**
   - NPC_1.json 파일의 구조 분석
   - 장면(Scene) 번호와 대화 흐름 이해하기
   - NPC 이름, 대사, 버튼, 명령어 설정 확인하기

3. **대화 시나리오 추가하기 (06:01-09:00)**
   - 새로운 대화 장면(Scene) 추가 방법
   - 복사-붙여넣기를 통한 효율적 장면 생성
   - 컨트롤+스페이스를 활용한 코드 자동 완성
   - 변수와 태그를 활용한 체계적인 대화 관리

4. **게임 내 적용 및 테스트 (09:01-끝)**
   - 애드온을 MC Addon 파일로 내보내기
   - 마인크래프트에서 NPC 소환 및 대화 테스트
   - 다양한 대화 분기 시나리오 확인하기
   - 대화에 따른 보상 시스템 작동 확인
   - 교육용 에디션 전용 기능 활용 방법

## 자주 묻는 질문

**Q: Bridge 프로그램은 어디서 다운로드 받을 수 있나요?**
A: 영상 설명란에 제공된 링크(https://youtu.be/L2s8-w8HXIk)를 통해 Bridge 프로그램 설치 영상을 시청하실 수 있습니다. Bridge는 마인크래프트 애드온 제작을 위한 무료 프로그램으로, 직관적인 인터페이스와 코드 자동 완성 기능을 제공합니다.

**Q: 대화형 NPC를 만들기 위해 꼭 Bridge 프로그램이 필요한가요?**
A: Bridge 프로그램이 필수는 아니지만, 복잡한 JSON 구조를 쉽게 편집하고 오류를 실시간으로 확인할 수 있어 매우 유용합니다. 텍스트 에디터로도 JSON 파일을 직접 편집할 수 있지만, 문법 오류 가능성이 높고 작업 효율이 떨어집니다. Bridge의 코드 자동 완성과 오류 검사 기능은 애드온 제작 시간을 크게 단축시켜 줍니다.

**Q: 만든 애드온을 다른 사람과 공유하려면 어떻게 해야 하나요?**
A: Bridge 프로그램에서 프로젝트를 작업한 후 '내보내기' 기능을 통해 .mcaddon 파일로 변환할 수 있습니다. 이 파일을 다른 사람에게 공유하면 상대방도 마인크래프트에서 해당 애드온을 사용할 수 있습니다. 베드락 에디션과 교육용 에디션 모두 동일한 방식으로 적용 가능하며, 영상에서 보여주는 방법대로 행동 팩과 리소스 팩을 모두 활성화해야 합니다.

## 추가 리소스
- [애드온 다운로드 링크(베드락, 교육용에디션)](https://o365cbe-my.sharepoint.com/:u:/g/personal/ssakspirit_o365cbe_net/EaCKelTqhqNFiBIw_u1me2gBDpw7pLTci-6k0UCKh1oWCw?e=dGTAyA)
- [송애정님의 dialogue 커맨드 설명 영상 1](https://youtu.be/vCNISHF5egg)
- [송애정님의 dialogue 커맨드 설명 영상 2](https://youtu.be/cq69gyc7bd8)
- [Bridge 설치 영상](https://youtu.be/L2s8-w8HXIk)
- [스티브 코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)

## 이런 분들에게 추천합니다
- 마인크래프트 월드에 스토리와 퀘스트를 추가하고 싶은 크리에이터
- 교육용 마인크래프트로 상호작용성 높은 학습 환경을 만들고 싶은 교육자
- 마인크래프트 애드온 제작에 관심이 있는 초중급 사용자
- 게임 내 대화 시스템과 스토리텔링에 관심 있는 게임 디자이너
- JSON 파일 구조를 통한 게임 컨텐츠 제작을 배우고 싶은 학습자

## 관련 튜토리얼
- [NPC 기본 사용법 알아보기]
- [Bridge 프로그램 사용 가이드]
- [마인크래프트 애드온 제작 기초]
- [JSON을 활용한 게임 컨텐츠 제작]
- [교육용 마인크래프트에서 퀘스트 시스템 구현하기]

## 실습 코드
```json
// NPC_1.json 파일 예시 코드

{
  "scene_1": {
    "npc_name": "스티브코딩",
    "text": "텍스트 게임을 좋아합니까?",
    "buttons": [
      {
        "name": "네! 좋아해요.",
        "commands": "/dialogue open @initiator scene_2"
      },
      {
        "name": "아니오",
        "commands": "/dialogue open @initiator scene_3"
      }
    ]
  },
  "scene_2": {
    "npc_name": "스티브코딩",
    "text": "어떤 게임을 좋아하세요?",
    "buttons": [
      {
        "name": "디아블로",
        "commands": "/dialogue open @initiator scene_4"
      },
      {
        "name": "문명",
        "commands": "/dialogue open @initiator scene_5"
      }
    ]
  },
  "scene_3": {
    "npc_name": "스티브코딩",
    "text": "그렇군요! 알겠습니다.",
    "buttons": [
      {
        "name": "끝내기",
        "commands": ""
      }
    ]
  },
  "scene_4": {
    "npc_name": "스티브코딩",
    "text": "디아블로를 좋아하시네요!",
    "buttons": [
      {
        "name": "디아블로 도끼 주세요",
        "commands": "/give @initiator iron_axe"
      },
      {
        "name": "디아블로 화살 주세요",
        "commands": "/give @initiator arrow 64"
      }
    ]
  },
  "scene_5": {
    "npc_name": "스티브코딩",
    "text": "문명을 좋아하시는군요!",
    "buttons": [
      {
        "name": "문명 추가 대화",
        "commands": "/dialogue open @initiator scene_6"
      }
    ]
  },
  "scene_6": {
    "npc_name": "스티브",
    "text": "만나서 반가웠어!",
    "buttons": [
      {
        "name": "나도 반가웠어",
        "commands": "/give @p apple"
      }
    ]
  }
}
```

## 태그
#마인크래프트 #NPC #대화시스템 #애드온제작 #브릿지 #베드락에디션 #교육용에디션 #퀘스트시스템 #게임디자인 #스토리텔링
