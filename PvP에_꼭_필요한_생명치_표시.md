---
title: "PvP에 꼭 필요한 생명치 표시"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/0sNQ9avt85Y/hqdefault.jpg"
tags: ["중급", "베드락", "스크립트", "설계자", "소스코드", "롱폼"]
url: "https://www.youtube.com/watch?v=0sNQ9avt85Y"
duration: "1:35"
series: "스크립트 API 시리즈"
episode: 0
difficulty: "중급"
---

# PvP에 꼭 필요한 생명치 표시

<div align="center">
<img src="https://i.ytimg.com/vi/0sNQ9avt85Y/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션에서 PvP 게임에 필수적인 생명력(HP) 표시 기능을 구현하는 방법을 알려줍니다. 스크립트 API를 활용하여 플레이어 머리 위에 현재 HP와 최대 HP를 표시하는 간단한 코드를 소개합니다. 이 기능은 PvP 게임에서 전략적인 플레이에 도움이 되는 중요한 요소입니다.

## 주요 내용

### 1. 생명력 표시 기능 소개
- 플레이어 이름 아래에 현재 HP/최대 HP 형식으로 표시
- 자신의 HP는 표시되지 않고 다른 플레이어의 HP만 확인 가능
- HP가 감소하거나 회복될 때 실시간으로 수치 변경

### 2. 스크립트 API 구현 방법
- 비교적 간단한 코드로 구현 가능
- 플레이어 컴포넌트를 가져와 현재 HP와 최대 HP 추출
- 플레이어 네임태그에 HP 정보 추가 표시

### 3. 코드 구조 및 원리
- 주기적으로 실행되는 반복 코드 사용
- 플레이어 컴포넌트에서 생명력 정보 가져오기
- 이름과 HP 표시를 위한 문자열 서식 설정

## 실습 과정

1. **기능 데모 (00:00-00:30)**
   - 알렉스 캐릭터의 이름 아래 HP 표시 확인
   - HP 감소 및 회복 시 실시간 업데이트 확인
   - 자신의 HP는 표시되지 않는 기능 확인

2. **코드 설명 (00:30-01:15)**
   - 간결한 스크립트 코드 소개
   - 반복 실행되는 코드 구조 설명
   - 플레이어 컴포넌트에서 HP 정보 추출 방법

3. **표시 형식 설명 (01:15-끝)**
   - 플레이어 이름 + 줄바꿈 + 현재 HP/최대 HP 형식
   - 분수 표현 방식(/)을 사용한 HP 표시
   - 실제 적용된 화면 확인

## 자주 묻는 질문

**Q: 이 코드는 교육용 에디션에서도 사용할 수 있나요?**
A: 이 코드는 베드락 에디션의 스크립트 API를 사용하므로 교육용 에디션에서는 직접 적용이 어려울 수 있습니다. 교육용 에디션에서는 대신 기본 명령어나 함수를 활용한 유사 기능 구현을 고려해보세요.

**Q: HP 표시 형식을 바꿀 수 있나요?**
A: 네, 코드에서 문자열 형식을 수정하여 표시 방식을 변경할 수 있습니다. 예를 들어 분수 대신 퍼센트로 표시하거나, 색상을 추가할 수도 있습니다.

**Q: 자신의 HP도 볼 수 있게 설정할 수 있나요?**
A: 코드를 수정하여 자신의 HP도 볼 수 있게 만들 수 있습니다. 현재 코드는 다른 플레이어의 HP만 표시하도록 설계되어 있습니다.

**Q: 이 코드는 서버에서도 작동하나요?**
A: 네, 이 스크립트를 포함한 행동 팩을 서버에 적용하면 모든 플레이어가 해당 기능을 사용할 수 있습니다.

## 추가 리소스
- [스크립트 API 시작하기 - 유튜브 가이드](https://youtu.be/zBVdaQ0AXOY)
- [GitHub에서 전체 코드 확인](https://github.com/ssakspirit/scriptAPI/blob/main/showHP.js)
- [마인크래프트 베드락 스크립트 API 공식 문서](https://learn.microsoft.com/en-us/minecraft/creator/scriptapi/minecraft/server/minecraft-server)
- [스티브코딩 채널](https://www.youtube.com/c/스티브코딩)

## 이런 분들에게 추천합니다
- PvP 게임 모드를 개발하는 마인크래프트 맵 제작자
- 스크립트 API를 배우고 싶은 마인크래프트 개발자
- PvP 게임에서 생명력 표시 기능이 필요한 서버 운영자
- 베드락 에디션에서 게임플레이 향상을 위한 기능을 추가하고 싶은 분

## 관련 튜토리얼
- [스크립트 API 시작하기](https://youtu.be/zBVdaQ0AXOY)
- [PvP에서 죽었을 때 부활하는 방법](링크)
- [PvP에서 킬 횟수 기록하기](링크)
- [PvP에서 활용하는 묘비 부활 시스템](링크)

## 실습 코드
```javascript
// 모든 플레이어에 대해 매 틱마다 실행
world.events.tick.subscribe(() => {
  for (const player of world.getPlayers()) {
    // 현재 HP와 최대 HP 가져오기
    const health = player.getComponent("health");
    const currentHP = health.currentValue;
    const maxHP = health.defaultValue;
    
    // 플레이어 이름 아래에 HP 표시
    player.nameTag = `${player.name}\n${currentHP}/${maxHP}`;
  }
});
```

## 태그
`#마인크래프트` `#베드락에디션` `#PvP` `#스크립트API` `#생명력표시` `#게임개발` `#스티브코딩`
