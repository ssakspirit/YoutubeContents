---
title: "PvP에서 활용하는 묘비 부활 시스템"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/BIV2JrK1GbE/hqdefault.jpg"
tags: ["고급", "베드락", "스크립트API", "소스코드", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=BIV2JrK1GbE"
duration: "3:32"
series: "스크립트 API 시리즈"
episode: 0
difficulty: "고급"
---

# PvP에서 활용하는 묘비 부활 시스템

<div align="center">
<img src="https://i.ytimg.com/vi/BIV2JrK1GbE/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션에서 PvP 게임을 위한 고급 묘비 부활 시스템을 구현하는 방법을 설명합니다. 스크립트 API를 활용하여 플레이어가 사망했을 때 묘비가 생성되고, 관전자 모드로 전환되며, 묘비를 파괴하거나 관리자 명령어를 통해 부활할 수 있는 기능을 구현합니다. 이 시스템은 PvP 게임의 재미와 전략적 요소를 높여주는 중요한 메커니즘입니다.

## 주요 내용

### 1. 묘비 부활 시스템 기능 소개
- 플레이어 사망 시 사망 위치에 묘비(아머 스탠드) 생성
- 사망한 플레이어는 관전자 모드로 자동 전환
- 관전자는 파티클 효과로 표시되며 전투에 참여 불가
- 묘비 파괴 시 해당 위치에서 부활

### 2. 관리자 부활 명령어 기능
- `!부활 [플레이어명]` 명령어로 관리자가 즉시 부활 가능
- 동시에 여러 플레이어 사망 시 각자의 묘비 생성
- 사망한 플레이어끼리는 서로 볼 수 있음

### 3. 코드 구조 및 원리
- 플레이어 데이터(위치, 이름 등)를 맵에 저장
- 이벤트 기반 시스템(사망, 묘비 파괴 등)
- 반복 실행 함수(RunInterval)를 통한 상태 관리
- 플레이어 퇴장 시 오류 방지를 위한 정리 코드

## 실습 과정

1. **기능 데모 (00:00-01:15)**
   - PvP 전투 시 플레이어 사망 및 묘비 생성 확인
   - 관전자 모드로 전환된 플레이어 이동 및 파티클 효과 확인
   - 묘비 파괴를 통한 부활 과정 시연

2. **관리자 명령어 시연 (01:15-01:50)**
   - `!부활 [플레이어명]` 명령어를 통한 강제 부활 기능 소개
   - 동시에 여러 플레이어 사망 시 각자의 묘비 생성 확인
   - 사망한 플레이어끼리 서로 확인 가능한 기능 시연

3. **코드 설명 (01:50-끝)**
   - 관리자 부활 명령어 코드 구조 설명
   - 플레이어 사망 이벤트 처리 코드 설명
   - 주기적으로 실행되는 함수(RunInterval)의 역할과 구조 설명
   - 플레이어 퇴장 시 오류 방지 코드 설명

## 자주 묻는 질문

**Q: 이 시스템은 어떤 마인크래프트 버전에서 작동하나요?**
A: 이 코드는 베드락 에디션의 스크립트 API를 사용하므로 최신 베드락 에디션에서 사용 가능합니다.

**Q: 묘비의 외형을 변경할 수 있나요?**
A: 네, 코드에서 아머 스탠드의 설정을 수정하여 묘비의 외형을 변경할 수 있습니다.

**Q: 부활 시 아이템을 잃게 되나요?**
A: 기본 설정에서는 아이템이 유지됩니다. 코드를 수정하여 사망 시 아이템을 드롭하거나 유지하도록 설정할 수 있습니다.

**Q: 이 시스템을 서버에 적용할 수 있나요?**
A: 네, 이 스크립트를 포함한 행동 팩을 서버에 적용하면 모든 플레이어가 해당 기능을 사용할 수 있습니다.

## 추가 리소스
- [스크립트 API 시작하기 - 유튜브 가이드](https://youtu.be/zBVdaQ0AXOY)
- [GitHub에서 전체 코드 확인](https://github.com/ssakspirit/scriptAPI)
- [마인크래프트 베드락 스크립트 API 공식 문서](https://learn.microsoft.com/en-us/minecraft/creator/scriptapi/minecraft/server/minecraft-server)
- [스티브코딩 채널](https://www.youtube.com/c/스티브코딩)

## 이런 분들에게 추천합니다
- PvP 게임 모드를 개발하는 마인크래프트 맵 제작자
- 스크립트 API의 고급 기능을 배우고 싶은 개발자
- 서버 운영자 및 관리자 기능을 개발하고 싶은 분
- 게임플레이 메커니즘에 전략적 요소를 추가하고 싶은 분

## 관련 튜토리얼
- [스크립트 API 시작하기](https://youtu.be/zBVdaQ0AXOY)
- [PvP에 꼭 필요한 생명치 표시](https://www.youtube.com/watch?v=0sNQ9avt85Y)
- [PvP에서 죽었을 때 부활하는 방법](https://www.youtube.com/watch?v=OyG4bP-rKpw)
- [PvP에서 킬 횟수 기록하기](https://www.youtube.com/watch?v=8ZmVK00xoLM)

## 실습 코드
```javascript
// 플레이어 데이터를 저장할 맵 객체
const playerGravesMap = new Map();
const playerIntervalsMap = new Map();

// 관리자 부활 명령어 처리
world.events.beforeChat.subscribe(chatEvent => {
  const message = chatEvent.message;
  if (message.startsWith("!부활 ")) {
    const playerName = message.substring(4).trim();
    const targetPlayer = [...world.getPlayers()].find(player => player.name === playerName);
    
    if (targetPlayer) {
      // 묘비 위치로 이동
      const graveLocation = playerGravesMap.get(playerName);
      targetPlayer.teleport(graveLocation);
      
      // 묘비(아머스탠드) 제거
      const grave = world.getDimension("overworld").getEntities({
        name: `${playerName}의 묘비`
      })[0];
      grave.kill();
      
      // 서바이벌 모드로 변경 및 이름 복원
      targetPlayer.setGameMode(GameMode.survival);
      targetPlayer.nameTag = playerName;
      world.sendMessage(`${playerName}님이 부활했습니다!`);
      
      // 파티클 효과 제거 및 플레이어 데이터 맵에서 삭제
      clearRunInterval(playerIntervalsMap.get(playerName));
      playerIntervalsMap.delete(playerName);
    }
  }
});

// 플레이어 사망 이벤트 처리
world.events.entityDie.subscribe(event => {
  const entity = event.entity;
  
  // 플레이어 사망 확인
  if (entity.typeId === "minecraft:player") {
    const player = entity;
    const playerName = player.name;
    
    // 관전자 모드로 변경
    player.setGameMode(GameMode.spectator);
    player.nameTag = `[사망] ${playerName}`;
    
    // 사망 위치 저장
    const deathLocation = player.location;
    playerGravesMap.set(playerName, deathLocation);
    
    // 묘비 생성 (아머스탠드)
    const grave = world.getDimension("overworld").spawnEntity("minecraft:armor_stand", deathLocation);
    grave.nameTag = `${playerName}의 묘비`;
    
    // 사망한 플레이어에게 파티클 효과 적용 (반복 실행)
    const intervalId = runInterval(() => {
      // 아머스탠드 존재 확인
      const armorStand = world.getDimension("overworld").getEntities({
        name: `${playerName}의 묘비`
      })[0];
      
      // 묘비가 파괴된 경우 부활
      if (!armorStand) {
        player.teleport(deathLocation);
        player.setGameMode(GameMode.survival);
        player.nameTag = playerName;
        world.sendMessage(`${playerName}님이 부활했습니다!`);
        clearRunInterval(intervalId);
        playerIntervalsMap.delete(playerName);
        return;
      }
      
      // 파티클 효과 지속
      const playerLocation = player.location;
      world.getDimension("overworld").spawnParticle(
        "minecraft:blue_flame_particle",
        playerLocation,
        new ParticleEffect()
      );
    }, 10);
    
    // 인터벌 ID 저장
    playerIntervalsMap.set(playerName, intervalId);
  }
});

// 플레이어 퇴장 시 정리
world.events.playerLeave.subscribe(event => {
  const player = event.player;
  const playerName = player.name;
  
  // 인터벌 있으면 제거
  if (playerIntervalsMap.has(playerName)) {
    clearRunInterval(playerIntervalsMap.get(playerName));
    playerIntervalsMap.delete(playerName);
  }
});
```

## 태그
`#마인크래프트` `#베드락에디션` `#PvP` `#스크립트API` `#부활시스템` `#게임개발` `#스티브코딩`
