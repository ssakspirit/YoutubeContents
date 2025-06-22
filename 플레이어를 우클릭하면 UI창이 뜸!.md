---
title: "플레이어를 우클릭하면 UI창이 뜸!"
date: "2025-04-26"
thumbnail: "https://i.ytimg.com/vi/axcJHzax5OU/hqdefault.jpg"
tags: ["중급", "베드락", "스크립트API", "소스코드", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=axcJHzax5OU"
duration: "4:50"
series: "마인크래프트 스크립트 API"
difficulty: "중급"
---

# 플레이어를 우클릭하면 UI창이 뜸!

<div align="center">
<img src="https://i.ytimg.com/vi/axcJHzax5OU/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션의 스크립트 API를 활용하여 플레이어를 우클릭했을 때 해당 플레이어의 정보(이름, 소지금, 레벨 등)를 보여주는 UI 창을 구현하는 방법을 설명합니다. 또한 채팅 명령어를 통해 자신의 정보를 확인하는 기능까지 포함하고 있습니다. 게임 내 RPG 요소나 멀티플레이어 상호작용 시스템을 제작하려는 개발자에게 유용한 튜토리얼입니다.

## 주요 내용

### 1. 플레이어 정보 UI 시스템 구현
- 우클릭 상호작용으로 다른 플레이어 정보 확인하기
- 채팅 명령어를 통한 자신의 정보 확인하기
- 스코어보드를 활용한 플레이어 데이터 관리

### 2. 스크립트 API 이벤트 활용법
- 플레이어 간 상호작용 이벤트 처리
- 채팅 이벤트 처리 및 명령어 시스템 구현
- UI 표시 타이밍 제어 및 사용자 상태 관리

### 3. UI 폼 디자인과 데이터 연동
- 동적 데이터를 표시하는 UI 폼 생성
- 스코어보드 값을 UI에 연동하는 방법
- 사용자 친화적인 UI 설계 원칙

## 실습 과정

1. **스코어보드 초기 설정 (00:00-01:00)**
   - 플레이어 우클릭 시 상호작용 테스트
   - 오류 메시지 확인 및 스코어보드 설정
   - '!스코어보드' 명령어로 초기화 진행

2. **플레이어 정보 확인 기능 테스트 (01:00-02:00)**
   - 다른 플레이어 우클릭으로 정보 확인하기
   - 스코어보드 값 변경 및 실시간 반영 확인
   - '!내정보' 명령어로 자신의 정보 확인하기

3. **코드 분석: 채팅 명령어 처리 (02:00-03:30)**
   - 채팅 이벤트 핸들러 구현 방법
   - 명령어 인식 및 함수 호출 구조
   - 스코어보드 초기화 코드 분석

4. **코드 분석: UI 폼 생성 및 표시 (03:30-끝)**
   - UI 폼 생성 및 구성 요소 설정
   - 스코어보드 값 조회 함수 구현
   - 플레이어 상호작용 이벤트 처리 방법

## 자주 묻는 질문

**Q: 이 스크립트는 어떤 버전의 마인크래프트에서 작동하나요?**  
A: 이 스크립트는 베드락 에디션에서 스크립트 API가 지원되는 버전(1.19.0 이상)에서 작동합니다. 자바 에디션에서는 사용할 수 없습니다.

**Q: 스코어보드 외에 다른 데이터도 UI에 표시할 수 있나요?**  
A: 네, 플레이어의 체력, 허기, 경험치, 인벤토리 아이템 등 스크립트 API에서 접근 가능한 모든 데이터를 UI에 표시할 수 있습니다. 영상의 코드를 확장하여 원하는 정보를 추가하면 됩니다.

**Q: 채팅 명령어 대신 다른 방법으로 자신의 정보를 확인할 수 있나요?**  
A: 물론입니다. 특정 아이템을 들고 우클릭하거나, 특정 블록을 클릭했을 때 정보가 표시되도록 이벤트 핸들러를 추가할 수 있습니다. 스크립트 API의 다양한 이벤트 핸들러를 활용하면 여러 상호작용 방식을 구현할 수 있습니다.

**Q: UI 디자인을 더 화려하게 만들 수 있나요?**  
A: 베드락 에디션의 스크립트 API에서 제공하는 UI 기능은 기본적인 폼 요소만 지원하여 디자인에 제한이 있습니다. 더 화려한 UI를 원한다면 HTML/CSS 같은 웹 기술을 활용한 외부 연동이나, 애드온을 통한 커스텀 UI를 개발해야 합니다.

## 추가 리소스

- [스크립트 API 시작하기](https://youtu.be/zBVdaQ0AXOY)
- [코드 다운로드 - GitHub](https://github.com/ssakspirit/scriptAPI/blob/main/UIinfo.js)
- [마인크래프트 베드락 에디션 스크립트 API 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/)
- [마인크래프트 폼 UI 튜토리얼](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/minecraft/server/formdata)
- [스코어보드 API 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/minecraft/server/scoreboard)

## 이런 분들에게 추천합니다

- 베드락 에디션에서 스크립트 API를 배우고자 하는 개발자
- 게임 내 RPG 시스템을 구현하려는 맵 제작자
- 플레이어 간 상호작용 기능을 추가하고 싶은 서버 운영자
- UI 시스템과 스코어보드를 연동하고 싶은 애드온 개발자
- 채팅 명령어 시스템을 구현하려는 프로그래머

## 관련 튜토리얼

- 스크립트 API 기본 사용법
- 스코어보드 시스템 구현하기
- 플레이어 상호작용 이벤트 처리
- 고급 UI 시스템 개발
- 베드락 에디션 애드온 제작

## 주요 코드 구조

```javascript
// 스코어보드 초기화
function initScoreboard() {
    const commands = [
        "scoreboard objectives add money dummy 소지금",
        "scoreboard objectives add level dummy 레벨",
        "scoreboard players set @a money 0",
        "scoreboard players set @a level 0",
        "tellraw @a {\"rawtext\":[{\"text\":\"머니와 레벨 값이 0으로 초기화 되었습니다.\"}]}"
    ];
    
    for (const command of commands) {
        world.getDimension("overworld").runCommand(command);
    }
}

// 플레이어 정보 표시 UI
function showPlayerInfo(source, target) {
    const form = new ModalFormData()
        .title("플레이어 정보")
        .textField("이름", "", target.name)
        .textField("소지금", "", getScore(target, "money"))
        .textField("레벨", "", getScore(target, "level"))
        .button("닫기");
        
    form.show(source).then(response => {
        // 폼 닫힘 처리
    }).catch(error => {
        // 사용자가 바쁜 경우 UI 표시 재시도
        if (error.message.includes("busy")) {
            world.system.runTimeout(() => {
                showPlayerInfo(source, target);
            }, 10);
        }
    });
}

// 스코어보드 값 가져오기
function getScore(entity, objective) {
    try {
        const scoreObj = world.scoreboard.getObjective(objective);
        if (scoreObj) {
            const score = scoreObj.getScore(entity.scoreboardIdentity);
            return score !== undefined ? score : "0";
        }
    } catch {
        return "0";
    }
    return "0";
}

// 채팅 명령어 핸들러
world.beforeEvents.chatSend.subscribe(event => {
    const player = event.sender;
    const message = event.message;
    
    if (message === "!스코어보드") {
        initScoreboard();
        event.cancel = true;
    } else if (message === "!내정보") {
        showMyInfo(player);
        event.cancel = true;
    }
});

// 플레이어 상호작용 이벤트 핸들러
world.beforeEvents.playerInteractWithEntity.subscribe(event => {
    const source = event.player;
    const target = event.target;
    
    if (target.typeId === "minecraft:player") {
        showPlayerInfo(source, target);
        event.cancel = true;
    }
});
```

## 태그
#마인크래프트 #베드락 #스크립트API #UI시스템 #플레이어정보 #스코어보드 #상호작용 #게임개발 #RPG시스템 #프로그래밍
