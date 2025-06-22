---
title: "아이템 배경 설명(lore) 정하기"
date: "2023-10-28"
thumbnail: "https://i.ytimg.com/vi/eeeDPiqHaVo/hqdefault.jpg"
tags: ["고급", "베드락", "스크립트API", "소스코드", "설계자", "롱폼", "커스텀", "아이템", "로어"]
url: "https://youtu.be/eeeDPiqHaVo"
duration: "1:56"
difficulty: "고급"
---

# 아이템 배경 설명(lore) 정하기

<div align="center">
<img src="https://i.ytimg.com/vi/eeeDPiqHaVo/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [로어(lore) 설명](#로어lore-설명)
- [사용 방법](#사용-방법)
- [코드 설명](#코드-설명)
- [실제 활용 방안](#실제-활용-방안)
- [다운로드 및 설치 방법](#다운로드-및-설치-방법)

## 소개
이 영상은 마인크래프트 베드락 에디션에서 스크립트 API를 활용하여 아이템에 배경 설명(lore)을 추가하는 방법을 설명합니다. 로어 기능을 사용하면 아이템에 특별한 설명을 추가하여 게임에 스토리텔링 요소를 더하거나 아이템의 특성을 더 자세히 설명할 수 있습니다.

## 로어(lore) 설명

### 로어란?
- 아이템에 대한 배경 설명이나 이야기를 추가하는 기능
- 일반 아이템에는 기본적으로 로어가 설정되어 있지 않음
- 사용자가 직접 정의하여 아이템에 개성과 특성 부여 가능

### 로어의 특징
- 아이템 설명 시 기본 정보 아래에 표시됨
- 여러 줄의 텍스트 추가 가능
- 아이템의 희귀성이나 특별한 스토리 부여 가능
- 게임 내 롤플레잉 요소로 활용 가능

## 사용 방법

### 로어 추가하기
1. 원하는 아이템을 손에 들고 있는 상태에서 채팅창 열기
2. `!로어 [설명 내용]` 형식으로 입력 (예: `!로어 이 검은 최초에 스티브 코딩이 사용했어요`)
3. 엔터를 누르면 "아이템의 로어가 추가 되었습니다" 메시지와 함께 설명 추가

### 로어 제거하기
1. 로어가 있는 아이템을 손에 들고 있는 상태에서 채팅창 열기
2. `!로어` 만 입력 (내용 없이)
3. 엔터를 누르면 "아이템의 로어가 제거 되었습니다" 메시지와 함께 설명 제거

### 사용 도움말 보기
- 올바르지 않은 형식으로 명령어를 입력하면 자동으로 사용법 안내

## 코드 설명

### 핵심 함수
- `getItemInMainHand()`: 플레이어가 손에 들고 있는 아이템 가져오기
- `setLore()`: 아이템에 로어 설정하기
- 채팅 이벤트 리스너: 채팅 명령어 감지 및 처리

### 주요 코드 구조
```javascript
// 채팅 이벤트 리스너
world.beforeEvents.chatSend.subscribe(chatEvent => {
  // 느낌표로 시작하는 명령어 감지
  if (chatEvent.message.startsWith("!로어")) {
    
    // 플레이어가 손에 들고 있는 아이템 가져오기
    const item = player.getItemInMainHand();
    
    // 아이템이 없는 경우 처리
    if (!item) return;
    
    // 로어 텍스트 추출
    const loreText = chatEvent.message.replace("!로어", "").trim();
    
    // 로어 제거 명령어인 경우
    if (loreText === "") {
      // 빈 배열로 설정하여 로어 제거
      newItem.setLore([]);
      player.sendMessage("아이템의 로어가 제거 되었습니다");
    } 
    // 로어 텍스트가 없는 경우 사용법 안내
    else if (!loreText) {
      player.sendMessage("사용법: !로어 [설명]");
    } 
    // 로어 추가
    else {
      // 새 로어 텍스트 설정
      newItem.setLore([loreText]);
      player.sendMessage("아이템의 로어가 추가 되었습니다");
    }
  }
});
```

## 실제 활용 방안

### 롤플레잉 서버
- 아이템에 역사와 배경 스토리 추가
- 퀘스트 아이템에 특별한 설명 부여
- NPC와 연결된 특별 아이템 설정

### 어드벤처 맵
- 단서나 힌트를 아이템 설명에 포함
- 아이템의 사용 방법 설명
- 스토리라인 요소 추가

### 멀티플레이어 서버
- 특별한 보상 아이템에 제작자 정보 추가
- 이벤트 참여 기념 아이템 설명
- 커스텀 상점 아이템 정보 제공

## 다운로드 및 설치 방법

### 필요 리소스
- [스크립트 API 시작하기](https://youtu.be/zBVdaQ0AXOY)
- [코드 다운로드](https://github.com/ssakspirit/scriptAPI/blob/main/setLore.js)
- [애드온 다운로드](https://o365cbe-my.sharepoint.com/:u:/g/personal/ssakspirit_o365cbe_net/ERAyXzVLYU5Jueb5SMYiwtYBQfMdGADTyaxq3MfVIR4mnA?e=7PnS7Q)

### 설치 방법
1. 스크립트 API 애드온 다운로드 및 설치
2. 제공된 코드를 프로젝트에 추가
3. 월드에 애드온 적용
4. 게임 내에서 명령어 사용

## 이런 분들에게 추천합니다
- 마인크래프트 서버 운영자
- 커스텀 맵 제작자
- 롤플레잉 서버 관리자
- 스크립트 API 학습에 관심 있는 개발자
- 아이템 커스터마이징을 좋아하는 플레이어

## 관련 자료
- [브릿지 가이드](https://youtu.be/L2s8-w8HXIk?si=aWJONVaLN0kngFtg)
- [베드락 공식 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/minecraft/server/minecraft-server)
- [스티브코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)