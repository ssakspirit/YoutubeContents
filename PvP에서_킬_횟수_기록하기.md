---
title: "PvP에서 킬 횟수 기록하기"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/CePqHZ83YBc/hqdefault.jpg"
tags: ["중급", "베드락", "스크립트API", "소스코드", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=CePqHZ83YBc"
duration: "3:08"
series: "스크립트 API 시리즈"
episode: 0
difficulty: "중급"
---

# PvP에서 킬 횟수 기록하기

<div align="center">
<img src="https://i.ytimg.com/vi/CePqHZ83YBc/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션에서 PvP 게임을 위한 킬 카운트 시스템을 구현하는 방법을 설명합니다. 스크립트 API를 활용하여 플레이어가 다른 플레이어를 처치할 때마다 자동으로 횟수를 기록하고 스코어보드에 표시하는 기능을 구현합니다. 채팅 명령어를 통해 카운터 시작 및 초기화도 가능한 유용한 PvP 게임 요소입니다.

## 주요 내용

### 1. 킬 카운트 시스템 기능 소개
- 플레이어가 다른 플레이어를 처치할 때마다 킬 횟수 자동 카운트
- 사이드바 스코어보드를 통한 킬 횟수 실시간 표시
- 채팅 명령어를 통한 카운터 시작 및 초기화 기능

### 2. 스크립트 API 구현 방법
- 스코어보드를 활용한 킬 카운트 저장 및 표시
- 채팅 이벤트를 통한 명령어 처리
- 엔티티 사망 이벤트를 활용한 킬 감지 및 카운팅

### 3. 코드 구조 및 원리
- 채팅 명령어 이벤트 처리 코드
- 엔티티 사망 이벤트 감지 및 처리
- 스코어보드 생성 및 관리 방법
- 조건문을 통한 플레이어 확인 로직

## 실습 과정

1. **킬 카운트 시스템 데모 (00:00-00:45)**
   - 채팅 명령어 '카운터'를 통해 시스템 시작
   - 스코어보드에 킬 카운트 표시 확인
   - 플레이어 처치 시 킬 카운트 증가 확인
   - '초기화' 명령어로 킬 카운트 리셋 시연

2. **코드 설명 (00:45-02:30)**
   - 채팅 명령어 처리 코드 설명
   - 스코어보드 생성 및 초기화 방법 설명
   - 엔티티 사망 이벤트 구독 및 처리 방법 설명
   - 킬 카운트 증가 로직 설명

3. **추가 기능 설명 (02:30-끝)**
   - 특정 이름을 가진 엔티티만 처리하는 조건문 추가 설명
   - 코드 활용 방법 및 응용 가능성 소개

## 자주 묻는 질문

**Q: 이 시스템은 어떤 마인크래프트 버전에서 작동하나요?**
A: 이 코드는 베드락 에디션의 스크립트 API를 사용하므로 최신 베드락 에디션에서 사용 가능합니다.

**Q: 킬 카운트를 리더보드 형식으로 정렬할 수 있나요?**
A: 네, 스코어보드 객체의 정렬 옵션을 수정하여 킬 수에 따른 리더보드를 구현할 수 있습니다.

**Q: 특정 무기로 킬했을 때만 카운트하도록 할 수 있나요?**
A: 네, 엔티티 사망 이벤트에서 추가 조건을 통해 특정 무기로 처치했을 때만 카운트하도록 코드를 수정할 수 있습니다.

**Q: 이 시스템을 서버에 적용할 수 있나요?**
A: 네, 이 스크립트를 포함한 행동 팩을 서버에 적용하면 모든 플레이어가 해당 기능을 사용할 수 있습니다.

## 추가 리소스
- [스크립트 API 시작하기 - 유튜브 가이드](https://youtu.be/zBVdaQ0AXOY)
- [GitHub에서 전체 코드 확인](https://github.com/ssakspirit/scriptAPI/blob/main/killCount.js)
- [마인크래프트 베드락 스크립트 API 공식 문서](https://learn.microsoft.com/en-us/minecraft/creator/scriptapi/minecraft/server/minecraft-server)
- [스티브코딩 채널](https://www.youtube.com/c/스티브코딩)

## 이런 분들에게 추천합니다
- PvP 게임 모드를 개발하는 마인크래프트 맵 제작자
- 스크립트 API의 기초를 배우고 싶은 개발자
- 서버 운영자 및 PvP 게임 설계자
- 킬 데스 기록이 필요한 서바이벌 게임 개발자

## 관련 튜토리얼
- [스크립트 API 시작하기](https://youtu.be/zBVdaQ0AXOY)
- [PvP에 꼭 필요한 생명치 표시](https://www.youtube.com/watch?v=0sNQ9avt85Y)
- [PvP에서 죽었을 때 부활하는 방법](https://www.youtube.com/watch?v=gQflxwqFkKo)
- [PvP에서 활용하는 묘비 부활 시스템](https://www.youtube.com/watch?v=BIV2JrK1GbE)

## 실습 코드
```javascript
// 킬 카운트 시스템 기본 코드
// 채팅 명령어 처리
world.events.beforeChat.subscribe(chatEvent => {
  const message = chatEvent.message;
  
  // 카운터 시작 명령어
  if (message === "카운터") {
    // 스코어보드 생성
    world.scoreboard.addObjective("킬", "킬 카운트");
    world.scoreboard.setObjectiveAtDisplaySlot(DisplaySlotId.sidebar, {
      objective: world.scoreboard.getObjective("킬")
    });
    
    // 모든 플레이어에게 초기값 설정
    for (const player of world.getPlayers()) {
      player.runCommand(`scoreboard players add @s 킬 0`);
    }
    
    chatEvent.sender.sendMessage("카운트를 시작합니다!");
    return;
  }
  
  // 초기화 명령어
  if (message === "초기화") {
    // 모든 플레이어의 킬 카운트 초기화
    for (const player of world.getPlayers()) {
      player.runCommand(`scoreboard players set @s 킬 0`);
    }
    
    chatEvent.sender.sendMessage("킬 카운트가 초기화되었습니다!");
    return;
  }
});

// 플레이어 사망 이벤트 처리
world.events.entityDie.subscribe(event => {
  const killerEntity = event.killer;
  const deadEntity = event.deadEntity;
  
  // 플레이어가 다른 플레이어를 처치한 경우만 처리
  if (killerEntity?.typeId === "minecraft:player" && deadEntity?.typeId === "minecraft:player") {
    const killer = killerEntity;
    const deadPlayer = deadEntity;
    
    // 처치 메시지 표시
    world.sendMessage(`${deadPlayer.name}님이 사망했습니다!`);
    
    // 킬 카운트 증가
    killer.runCommand(`scoreboard players add @s 킬 1`);
  }
  
  // 특정 이름의 엔티티 처리 예시 (선택적 추가 기능)
  // if (killerEntity?.typeId === "minecraft:player" && deadEntity?.name === "특정몹이름") {
  //   const killer = killerEntity;
  //   killer.runCommand(`scoreboard players add @s 킬 1`);
  // }
});

// 플레이어 참가 이벤트 - 새로운 플레이어 킬 카운트 초기화
world.events.playerJoin.subscribe(event => {
  const player = event.player;
  try {
    // 스코어보드가 존재하면 새 플레이어에게 초기값 설정
    player.runCommand(`scoreboard players add @s 킬 0`);
  } catch (e) {
    // 스코어보드가 아직 없는 경우 (예외 처리)
  }
});
```

## 태그
`#마인크래프트` `#베드락에디션` `#PvP` `#스크립트API` `#킬카운트` `#게임개발` `#스티브코딩`
