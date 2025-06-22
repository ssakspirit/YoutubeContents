---
title: "블록과 상호작용하면 UI창이 뜬다!"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/vNNOwEbXfRo/hqdefault.jpg"
tags: ["중급", "베드락", "스크립트API", "소스코드", "설계자", "롱폼"]
url: "https://youtu.be/vNNOwEbXfRo"
duration: "2:10"
series: "마인크래프트 스크립트 API"
difficulty: "중급"
---

# 블록과 상호작용하면 UI창이 뜬다!

<div align="center">
<img src="https://i.ytimg.com/vi/vNNOwEbXfRo/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션에서 스크립트 API를 활용하여 블록과 상호작용할 때 UI창이 나타나는 기능을 구현하는 방법을 소개합니다. 다이아몬드 블록, 에메랄드 블록 등 특정 블록을 빈 손으로 우클릭하면 커스텀 UI 메뉴가 표시되고, 해당 메뉴에서 다양한 기능을 실행할 수 있는 시스템의 제작 과정을 설명합니다.

## 주요 내용

### 1. 블록 상호작용 시스템 개요
- 빈 손으로 특정 블록을 우클릭하면 UI창 표시
- 블록 종류에 따라 다른 메뉴 및 기능 제공
- 아이템을 들고 있으면 기존 블록 설치 기능이 우선됨
- 상호작용 가능한 블록 종류 확장 가능

### 2. UI 창 구성 요소
- 블록 이름을 활용한 UI 창 제목 설정
- 블록 종류별 고유 메뉴 타이틀 설정
- 버튼 텍스트와 아이콘 커스터마이징
- 버튼 클릭 시 실행되는 명령어 연결

### 3. 코드 구조 및 확장 방법
- 블록 종류에 따른 케이스별 UI 설정
- 상호작용 이벤트 처리 시스템
- 맨손 상태 확인 조건문
- 새로운 블록 타입 추가 방법

## 실습 과정

1. **기본 기능 확인 (00:00-00:40)**
   - 다이아몬드 블록과 에메랄드 블록 상호작용 테스트
   - 빈 손으로 블록 우클릭하여 UI창 확인
   - 블록별 다른 메뉴와 기능 확인
   - 아이템 들고 있을 때 기존 기능 유지됨을 확인

2. **코드 구조 분석 (00:41-01:20)**
   - UI창 구현 코드 설명
   - 블록 이름을 활용한 UI 제목 설정 방식
   - 버튼 구성과 아이콘 설정 부분 설명
   - 케이스별 처리 구조 확인

3. **새 블록 추가 방법 (01:21-끝)**
   - 골드 블록을 위한 새 UI 메뉴 추가
   - 코드 복사 및 수정 과정
   - 상호작용 이벤트 처리 코드 추가
   - 완성된 시스템 테스트

## 자주 묻는 질문

**Q: 이 기능을 구현하기 위해 필요한 사전 지식이 있나요?**
A: 마인크래프트 베드락 에디션의 스크립트 API에 대한 기본 이해가 필요합니다. 영상 설명란에 있는 "스크립트 API 시작하기" 영상을 먼저 시청하시는 것이 좋습니다.

**Q: 어떤 종류의 블록에 이 기능을 추가할 수 있나요?**
A: 원칙적으로 모든 블록에 이 기능을 추가할 수 있습니다. 다만, 문이나 버튼처럼 자체적으로 상호작용 기능이 있는 블록은 기존 기능과 충돌할 수 있으므로 주의해야 합니다.

**Q: UI 창에 추가할 수 있는 최대 버튼 수가 정해져 있나요?**
A: 명확한 제한은 없지만, 화면 크기를 고려하여 적절한 수의 버튼을 배치하는 것이 좋습니다. 일반적으로 3-6개 정도의 버튼이 가독성 측면에서 이상적입니다.

**Q: 버튼 클릭 시 어떤 종류의 명령을 실행할 수 있나요?**
A: 게임 내 효과 부여, 아이템 지급, 텔레포트, 게임 모드 변경 등 대부분의 명령어를 실행할 수 있습니다. 또한 스크립트 내에서 복잡한 로직이나 함수를 실행하는 것도 가능합니다.

## 추가 리소스
- [스크립트 API 시작하기](https://youtu.be/zBVdaQ0AXOY)
- [코드 다운로드 (GitHub)](https://github.com/ssakspirit/scriptAPI/blob/main/interactiveBlockMenuSystem.js)
- [브릿지 가이드](https://youtu.be/L2s8-w8HXIk?si=aWJONVaLN0kngFtg)
- [베드락 공식 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/minecraft/server/minecraft-server)
- [스티브코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)

## 이런 분들에게 추천합니다
- 마인크래프트 베드락 에디션에서 고급 기능을 구현하고 싶은 개발자
- 서버나 월드에 상호작용 요소를 추가하고 싶은 맵 제작자
- 스크립트 API를 활용한 실용적인 예제를 찾고 있는 학습자
- 퀘스트나 미니게임에 UI 요소를 추가하고 싶은 콘텐츠 제작자
- 기존 블록에 추가 기능을 부여하고 싶은 애드온 개발자

## 관련 튜토리얼
- 스크립트 API로 본격적으로 애드온 제작하기
- 스크립트 API의 첫걸음, 채팅명령어 만들기
- 플레이어를 우클릭하면 UI창이 뜸!
- 언제 어디든 아이템을 살 수 있는 UI 상점
- 블록을 캐는 것이 아닌 상호작용하는 방법

## 실습 코드
```javascript
// 블록과 상호작용 시 UI창 표시 이벤트 처리
import { world, ItemStack, BlockInventoryComponent, ItemTypes, system, BlockPermutation } from "@minecraft/server";
import { ActionFormData, ModalFormData } from "@minecraft/server-ui";

// 블록 상호작용 이벤트 처리
world.events.beforeItemUseOn.subscribe((eventData) => {
    const player = eventData.source;
    const block = player.dimension.getBlock(eventData.blockLocation);
    const item = eventData.item;
    
    // 맨손으로 상호작용할 때만 UI 표시
    if (item?.typeId === undefined) {
        // 다이아몬드 블록
        if (block.typeId === "minecraft:diamond_block") {
            eventData.cancel = true;
            showBlockUI(player, "diamond_block");
        }
        // 에메랄드 블록
        else if (block.typeId === "minecraft:emerald_block") {
            eventData.cancel = true;
            showBlockUI(player, "emerald_block");
        }
        // 골드 블록 (확장 예시)
        else if (block.typeId === "minecraft:gold_block") {
            eventData.cancel = true;
            showBlockUI(player, "gold_block");
        }
    }
});

// UI 표시 함수
function showBlockUI(player, blockType) {
    const form = new ActionFormData();
    const blockName = blockType.replace("minecraft:", "").replace("_block", " 블록");
    
    form.title(blockName.charAt(0).toUpperCase() + blockName.slice(1));
    
    switch (blockType) {
        case "diamond_block":
            form.body("다이아몬드블록 메뉴");
            form.button("점프 부스트", "textures/items/diamond");
            form.button("속도 부스트", "textures/items/diamond_boots");
            form.button("야간 투시", "textures/items/diamond_helmet");
            break;
        
        case "emerald_block":
            form.body("에메랄드블록 메뉴");
            form.button("체력 회복", "textures/items/emerald");
            form.button("허기 회복", "textures/items/apple");
            form.button("보호막 부여", "textures/items/emerald_chestplate");
            break;
            
        case "gold_block":
            form.body("골드블록 메뉴");
            form.button("공중부양", "textures/items/gold_ingot");
            form.button("행운 부여", "textures/items/gold_horse_armor");
            form.button("황금 물품 지급", "textures/blocks/gold_block");
            break;
    }
    
    form.show(player).then((response) => {
        if (response.canceled) return;
        
        if (blockType === "diamond_block") {
            switch (response.selection) {
                case 0: // 점프 부스트
                    player.runCommand(`effect @s jump_boost 30 1 true`);
                    break;
                case 1: // 속도 부스트
                    player.runCommand(`effect @s speed 30 1 true`);
                    break;
                case 2: // 야간 투시
                    player.runCommand(`effect @s night_vision 60 0 true`);
                    break;
            }
        }
        else if (blockType === "emerald_block") {
            switch (response.selection) {
                case 0: // 체력 회복
                    player.runCommand(`effect @s instant_health 1 1 true`);
                    break;
                case 1: // 허기 회복
                    player.runCommand(`effect @s saturation 1 10 true`);
                    break;
                case 2: // 보호막 부여
                    player.runCommand(`effect @s resistance 60 1 true`);
                    break;
            }
        }
        else if (blockType === "gold_block") {
            switch (response.selection) {
                case 0: // 공중부양
                    player.runCommand(`effect @s levitation 10 1 true`);
                    break;
                case 1: // 행운 부여
                    player.runCommand(`effect @s luck 120 2 true`);
                    break;
                case 2: // 황금 물품 지급
                    player.runCommand(`give @s gold_ingot 5`);
                    break;
            }
        }
    });
}
```

## 태그
#마인크래프트 #베드락 #스크립트API #UI #상호작용 #블록기능 #커스텀UI #애드온제작 #게임개발 #사용자인터페이스
