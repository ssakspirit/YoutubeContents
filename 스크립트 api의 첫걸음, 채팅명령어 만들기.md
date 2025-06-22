---
title: "스크립트 api의 첫걸음, 채팅명령어 만들기 #애드온제작"
date: "2025-04-26"
thumbnail: "https://i.ytimg.com/vi/gWSHwuKR_Vk/hqdefault.jpg"
tags: ["초급", "베드락", "스크립트API", "소스코드", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=gWSHwuKR_Vk"
duration: "5:00"
series: "애드온 제작 튜토리얼"
difficulty: "초급"
---

# 스크립트 api의 첫걸음, 채팅명령어 만들기

<div align="center">
<img src="https://i.ytimg.com/vi/gWSHwuKR_Vk/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션에서 스크립트 API를 활용하여 채팅창에 입력하는 명령어를 만드는 방법을 소개합니다. 기존의 function 명령어와 달리 슬래시(/)를 사용하지 않고 일반 채팅처럼 입력할 수 있는 커스텀 명령어를 제작하는 과정을 단계별로 설명합니다. 브릿지(Bridge) 프로그램을 활용하여 초보자도 쉽게 따라할 수 있는 기본적인 스크립트 API 활용법을 배울 수 있습니다.

## 주요 내용

### 1. 스크립트 API와 채팅명령어 개요
- 일반 채팅 메시지로 작동하는 명령어의 특징
- function 명령어와의 차이점 설명
- 스크립트 API의 기초 개념 이해하기

### 2. 개발 환경 설정
- 브릿지(Bridge) 프로그램 설치 및 활용 방법
- 새 프로젝트 생성 및 기본 설정
- 마인크래프트 버전 설정 및 스크립트 API 활성화

### 3. 채팅명령어 스크립트 작성
- 기본 스크립트 구조 이해하기
- 이벤트 리스너를 활용한 채팅 메시지 감지
- 다중 명령어 설정 및 복합 기능 구현

## 실습 과정

1. **개발 환경 준비 (00:00-01:30)**
   - 브릿지(Bridge) 프로그램 실행
   - 새 프로젝트 생성 시 옵션 선택:
     - 행동 팩 활성화 (리소스 팩은 선택사항)
     - 월드 내보내기 옵션 활성화
     - 베타 API 옵션 반드시 활성화
   - 프로젝트 이름 설정 및 버전 선택 (교육용 에디션의 경우 낮은 버전 선택)

2. **초기 스크립트 테스트 (01:31-03:20)**
   - 기본 콘솔 메시지 작성:
   ```javascript
   console.warn("Hello");
   ```
   - 마인크래프트에서 행동 팩 적용 및 실험 기능 활성화
   - 오류 발생 시 매니페스트 파일에서 버전 수정:
     - "minecraft_server": "1.7.0"
     - "minecraft_server_ui": "1.2.0"
   - 수정 후 다시 로드하여 정상 작동 확인

3. **채팅명령어 스크립트 작성 (03:21-04:30)**
   - main.js 파일에 다음 코드 작성:
   ```javascript
   import { world } from "@minecraft/server";

   // 채팅 이벤트 리스너 등록
   world.beforeEvents.chatSend.subscribe((chatEvent) => {
     const message = chatEvent.message;

     // 명령어 1 감지 및 실행
     if (message === "명령어1") {
       chatEvent.sender.runCommandAsync(`tellraw @a {"rawtext":[{"text":"명령어 1을 실행함"}]}`);
       chatEvent.cancel = true;
     }

     // 명령어 2 감지 및 실행 (여러 명령어 실행)
     if (message === "명령어2") {
       chatEvent.sender.runCommandAsync(`tellraw @a {"rawtext":[{"text":"명령어 2를 실행함"}]}`);
       chatEvent.sender.runCommandAsync(`give @s apple 2`);
       chatEvent.cancel = true;
     }

     // 명령어 3 감지 및 실행
     if (message === "명령어3") {
       chatEvent.sender.runCommandAsync(`effect @s speed 10 1 true`);
       chatEvent.cancel = true;
     }
   });
   ```
   - 저장 후 마인크래프트에서 `/reload` 명령어로 적용

4. **채팅명령어 테스트 및 내보내기 (04:31-끝)**
   - 채팅창에 "명령어1", "명령어2", "명령어3" 입력하여 기능 확인
   - 애드온으로 내보내기: "..." 메뉴에서 "애드온으로 내보내기" 선택
   - .mcaddon 파일을 생성하여 교육용 에디션에서도 사용 가능

## 자주 묻는 질문

**Q: 교육용 에디션에서도 이 방법을 사용할 수 있나요?**
A: 네, 사용할 수 있습니다. 교육용 에디션에서 적용하려면 브릿지에서 애드온으로 내보내기를 한 후, .mcaddon 파일을 교육용 에디션에서 열면 됩니다. 다만 실험 기능 메뉴가 보이지 않을 수 있어 추가 애드온을 사용해야 할 수 있습니다. 관련 튜토리얼은 영상 설명란에서 확인할 수 있습니다.

**Q: 명령어 이름을 한글로 해도 되나요?**
A: 네, 한글로 명령어를 지정해도 정상적으로 작동합니다. 영상에서도 "명령어1", "명령어2", "명령어3"과 같이 한글 명령어를 사용했습니다.

**Q: 채팅명령어에 매개변수를 추가할 수 있나요?**
A: 네, 가능합니다. 예를 들어 "텔레포트 x y z" 형식으로 명령어를 만들고 싶다면, chatEvent.message를 파싱하여 공백으로 분리한 후 각 값을 추출하여 사용할 수 있습니다. 이는 보다 고급 스크립팅 기술이 필요합니다.

**Q: 명령어가 실행되면서 채팅에 보이는 것을 막을 수 있나요?**
A: 네, 코드에서 `chatEvent.cancel = true;` 부분이 바로 그 역할을 합니다. 이 코드가 있으면 명령어가 채팅창에 표시되지 않고 바로 실행됩니다.

## 추가 리소스
- [스크립트 API 시작하기](https://youtu.be/zBVdaQ0AXOY)
- [브릿지 가이드](https://youtu.be/L2s8-w8HXIk?si=aWJONVaLN0kngFtg)
- [베드락 공식 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/minecraft/server/minecraft-server)
- [스티브코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)

## 이런 분들에게 추천합니다
- 마인크래프트 베드락에서 커스텀 명령어를 만들고 싶은 초보 개발자
- 스크립트 API를 처음 접하는 마인크래프트 애드온 제작자
- 채팅 인터페이스를 통해 게임 기능을 제어하고 싶은 월드 제작자
- 기존의 명령어 블록이나 function 파일로는 구현하기 어려운 기능을 만들고 싶은 사용자
- 자바스크립트를 활용하여 마인크래프트를 확장하고 싶은 프로그래머

## 관련 튜토리얼
- 스크립트 API로 본격적으로 애드온 제작하기 #애드온제작
- 스크립트 API영상의 코드를 이렇게 애드온으로 바꾸세요
- 애드온 제작을 한다면 꼭 필요한 몇 가지! #애드온제작튜토리얼
- 채팅명령어와 함수는 구별해서 사용해야 해요! #코드작성기튜토리얼

## 실습 코드
```javascript
// 필수 모듈 임포트
import { world } from "@minecraft/server";

// 채팅 이벤트 리스너 등록
world.beforeEvents.chatSend.subscribe((chatEvent) => {
  const message = chatEvent.message;

  // 명령어 1 감지 및 실행
  if (message === "명령어1") {
    chatEvent.sender.runCommandAsync(`tellraw @a {"rawtext":[{"text":"명령어 1을 실행함"}]}`);
    chatEvent.cancel = true;
  }

  // 명령어 2 감지 및 실행 (여러 명령어 실행)
  if (message === "명령어2") {
    chatEvent.sender.runCommandAsync(`tellraw @a {"rawtext":[{"text":"명령어 2를 실행함"}]}`);
    chatEvent.sender.runCommandAsync(`give @s apple 2`);
    chatEvent.cancel = true;
  }

  // 명령어 3 감지 및 실행
  if (message === "명령어3") {
    chatEvent.sender.runCommandAsync(`effect @s speed 10 1 true`);
    chatEvent.cancel = true;
  }
});
```

## 태그
#마인크래프트 #베드락에디션 #스크립트API #애드온제작 #채팅명령어 #자바스크립트 #브릿지 #게임개발 #코딩 #스티브코딩