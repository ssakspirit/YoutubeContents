---
title: "마인크래프트 애드온 제작툴 「bridge」 셋팅 방법! #애드온제작튜토리얼"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/L2s8-w8HXIk/hqdefault.jpg"
tags: ["초급", "베드락", "가이드", "애드온제작", "서드파티", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=L2s8-w8HXIk"
duration: "6:55"
difficulty: "초급"
---

# 마인크래프트 애드온 제작툴 「bridge」 셋팅 방법! #애드온제작튜토리얼

<div align="center">
<img src="https://i.ytimg.com/vi/L2s8-w8HXIk/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션과 에듀케이션 에디션에서 사용할 수 있는 애드온 제작 도구인 bridge의 설치 및 기본 셋팅 방법을 안내합니다. bridge는 복잡한 JSON 파일 편집을 시각적이고 직관적인 인터페이스로 제공하여 애드온 제작을 쉽게 만들어주는 도구입니다. 이 툴을 통해 리소스팩과 행동팩을 효율적으로 만들 수 있는 기본 환경 설정 방법을 배울 수 있습니다.

## 주요 내용

### 1. bridge 설치 및 초기 설정
- bridge 웹사이트 접속 및 프로그램 설치 방법
- 프로젝트 폴더 및 com.mojang 폴더 연결 설정
- 트리 형태와 텍스트 형태의 편집 모드 선택 및 전환 방법

### 2. 새 프로젝트 생성 및 설정
- 행동팩(Behavior Pack)과 리소스팩(Resource Pack) 설정
- 프로젝트 이름, 설명, 프리픽스 등 기본 정보 설정
- 실험적 게임플레이 옵션 및 대상 버전 설정
- 제작자 정보 입력 및 매니페스트 파일 생성

### 3. bridge의 주요 기능 및 장점
- 자동 문법 체크 및 가이드 제공
- com.mojang 폴더와의 자동 동기화 기능
- 문서화된 컴포넌트 접근 및 도움말 제공
- JSON 파일 편집을 위한 직관적 인터페이스

## 실습 과정

1. **bridge 설치 (00:00-01:30)**
   - "bridge Minecraft" 검색하여 웹사이트 접속
   - 웹 에디터 또는 데스크톱 앱 설치 선택
   - 프로젝트 저장 폴더 지정
   - com.mojang 폴더 연결 설정 (선택사항이지만 권장)

2. **새 프로젝트 생성 (01:31-03:20)**
   - New Project 버튼으로 새 프로젝트 시작
   - 행동팩(BP)과 리소스팩(RP) 선택
   - 프로젝트 이름, 설명, 썸네일 설정
   - 프로젝트 프리픽스 설정 (블록, 엔티티 등에 자동 적용)
   - 제작자 정보 및 최소 필요 게임 버전 설정 (1.17 권장)

3. **기본 파일 구조 이해 (03:21-04:40)**
   - 생성된 프로젝트 구조 탐색
   - 블록 등 새 요소 추가 테스트
   - 자동으로 생성되는 JSON 파일 구조 확인
   - com.mojang 폴더와 동기화 확인

4. **bridge 편집 기능 시연 (04:41-끝)**
   - 블록 속성 편집 인터페이스 사용법
   - 컴포넌트 문서 확인 방법 (우클릭 > View Documentation)
   - 트리 형태와 텍스트 형태 편집 모드 전환
   - 수정한 내용 마인크래프트에서 바로 확인하기

## 자주 묻는 질문

**Q: bridge를 사용하려면 어떤 마인크래프트 버전이 필요한가요?**
A: bridge는 마인크래프트 베드락 에디션과 교육용 에디션에서 사용 가능합니다. 자바 에디션에서는 사용할 수 없습니다. 프로젝트 생성 시 대상 버전을 설정할 수 있으며, 영상에서는 1.17 버전을 권장합니다.

**Q: com.mojang 폴더는 어디에 있나요?**
A: 베드락 에디션의 경우 일반적으로 `C:\Users\사용자이름\AppData\Local\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang` 경로에 있습니다. 교육용 에디션은 `C:\Users\사용자이름\AppData\Roaming\Minecraft Education Edition\games\com.mojang` 경로에 있습니다. 정확한 경로는 영상 설명란에도 기재되어 있습니다.

**Q: bridge로 만든 애드온을 다른 사람과 공유하려면 어떻게 해야 하나요?**
A: bridge 프로젝트 폴더에 생성된 파일을 .mcpack 또는 .mcaddon 형태로 내보내거나, com.mojang 폴더 내의 해당 프로젝트 행동팩/리소스팩 폴더를 압축하여 공유할 수 있습니다.

**Q: bridge의 트리 형태와 텍스트 형태 중 어떤 것을 사용하는 것이 좋을까요?**
A: 초보자라면 트리 형태가 직관적이고 쉽게 사용할 수 있어 권장됩니다. 텍스트 형태는 JSON 파일을 직접 수정하는 데 익숙한 사용자나 복잡한 편집이 필요할 때 유용합니다. 두 가지 형태는 언제든지 전환하여 사용할 수 있습니다.

## 추가 리소스
- [bridge 공식 웹사이트](https://bridge-core.app/)
- [마인크래프트 베드락 에디션 애드온 문서](https://docs.microsoft.com/minecraft/creator/)
- [베드락 에디션 com.mojang 폴더 경로](C:\Users\사용자이름\AppData\Local\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang)
- [교육용 에디션 com.mojang 폴더 경로](C:\Users\사용자이름\AppData\Roaming\Minecraft Education Edition\games\com.mojang)

## 실습 코드
```json
// 기본 블록 JSON 예시 (test.json)
{
  "format_version": "1.16.100",
  "minecraft:block": {
    "description": {
      "identifier": "abc:test",
      "register_to_creative_menu": true
    },
    "components": {
      "minecraft:loot": "loot_tables/blocks/test.json",
      "minecraft:destroy_time": 0.5,
      "minecraft:explosion_resistance": 1,
      "minecraft:friction": 0.6,
      "minecraft:flammable": {
        "flame_odds": 0,
        "burn_odds": 0
      }
    }
  }
}
```

## 이런 분들에게 추천합니다
- 마인크래프트 애드온 제작에 관심이 있으나 복잡한 JSON 편집에 어려움을 느끼는 초보자
- 기존 텍스트 에디터 대신 더 효율적인 애드온 제작 도구를 찾고 있는 사용자
- 베드락 에디션이나 교육용 에디션을 위한 커스텀 컨텐츠를 만들고 싶은 교육자
- 시각적 인터페이스를 통해 애드온 개발을 배우고 싶은 학생
- 자신만의 블록, 아이템, 엔티티 등을 만들어 마인크래프트 세계를 확장하고 싶은 모든 사용자

## 관련 튜토리얼
- [마인크래프트 애드온 제작! 이보다 더 쉬운 방법 없습니다.](https://www.youtube.com/watch?v=2T__ACTCNFk)
- [애드온 제작을 한다면 꼭 필요한 몇 가지! #애드온제작튜토리얼](https://www.youtube.com/watch?v=...)
- [스크립트 API로 본격적으로 애드온 제작하기 #애드온제작](https://www.youtube.com/watch?v=...)
- [말이 많은 NPC 만들기! #애드온제작튜토리얼](https://www.youtube.com/watch?v=...)

## 태그
`#마인크래프트` `#애드온제작` `#bridge` `#베드락에디션` `#에듀케이션에디션` `#JSON` `#행동팩` `#리소스팩` `#모드제작` `#스티브코딩`