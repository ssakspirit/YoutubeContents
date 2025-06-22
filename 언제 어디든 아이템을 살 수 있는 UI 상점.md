---
title: "언제 어디든 아이템을 살 수 있는 UI 상점"
date: "2025-04-26"
thumbnail: "https://i.ytimg.com/vi/HkYCHQu0dmw/hqdefault.jpg"
tags: ["고급", "베드락", "스크립트API", "소스코드", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=HkYCHQu0dmw"
duration: "2:56"
series: "스크립트 API 튜토리얼"
episode: null
difficulty: "고급"
---

# 언제 어디든 아이템을 살 수 있는 UI 상점

<div align="center">
<img src="https://i.ytimg.com/vi/HkYCHQu0dmw/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션의 스크립트 API를 활용하여 UI 기반의 상점 시스템을 구현하는 방법을 소개합니다. 이 시스템을 통해 플레이어는 특정 아이템(나침반)을 들고 우클릭하면 언제 어디서든 상점 UI가 열리고, 에메랄드를 화폐로 사용하여 다양한 아이템을 구매할 수 있습니다. 상점 UI는 직관적인 인터페이스를 제공하며, 아이템별 가격이 표시되고 구매 수량을 조절할 수 있는 기능을 포함합니다. 또한 새로운 상품을 쉽게 추가할 수 있는 확장 가능한 코드 구조를 가지고 있어, 서버 운영자나 월드 제작자가 자신만의 커스텀 상점을 쉽게 구현할 수 있습니다.

## 주요 내용

### 1. UI 상점 시스템 구현 개요
- 나침반 아이템을 사용한 상점 접근 방식
- 에메랄드를 통한 결제 시스템
- 아이템 종류와 가격 설정 방법
- 구매 수량 조절 기능

### 2. 상점 UI 디자인 및 기능
- 시각적인 아이템 표시와 가격 정보
- 수량 선택 슬라이더 구현
- 구매 버튼 및 트랜잭션 처리
- 인벤토리 관리 및 아이템 지급 메커니즘

### 3. 코드 커스터마이징 방법
- 새로운 상품 추가 방법
- 아이템 가격 설정 방법
- UI 텍스트 및 표시 방식 수정
- 명령어 처리 로직 이해

### 4. 리로드 및 업데이트 프로세스
- 코드 수정 후 리로드 방법
- 동적으로 상점 내용 업데이트하기
- 테스트 및 디버깅 접근법

## 실습 과정

1. **UI 상점 기본 기능 시연 (00:00-00:45)**
   - 나침반 아이템 우클릭으로 상점 UI 열기
   - 황금 사과(3 에메랄드), 감자(2 에메랄드), 당근(1 에메랄드) 가격 확인
   - 수량 선택 기능 및 구매 버튼 설명
   - 구매 시 에메랄드 차감 및 아이템 획득 과정 확인

2. **구매 테스트 및 UI 작동 방식 (00:45-01:15)**
   - 황금 사과 1개 구매 테스트
   - 감자 5개 구매 테스트(10 에메랄드 차감)
   - 당근 10개 구매 테스트(10 에메랄드 차감)
   - 인벤토리 확인 및 정확한 거래 처리 확인

3. **코드 구조 및 커스터마이징 방법 (01:15-02:40)**
   - 상점 아이템 정의 부분 설명
   - 아이템 가격 설정 코드 분석
   - 새로운 아이템(사과) 추가 방법 시연
   - 아이템 이름 설정 및 코드 저장 방법

4. **리로드 및 테스트 (02:40-02:56)**
   - 행동 팩 리로드 명령어 실행
   - 수정된 상점 열어 새 아이템(사과) 확인
   - 사과 10개 구매 테스트 및 결과 확인
   - 최종 기능 확인 및 영상 마무리

## 자주 묻는 질문

**Q: 이 기능을 구현하기 위해 필요한 기술적 지식 수준은 어느 정도인가요?**
A: 이 기능은 마인크래프트 베드락 에디션의 스크립트 API를 활용하므로, JavaScript에 대한 기본적인 이해가 필요합니다. 완전 초보자에게는 다소 어려울 수 있으나, 영상에서 제공되는 GitHub 코드를 활용하면 프로그래밍 경험이 적더라도 충분히 구현 가능합니다. 코드를 수정하여 새 아이템을 추가하는 정도는 간단한 코드 편집만으로도 가능합니다.

**Q: 상점에서 판매할 수 있는 아이템에 제한이 있나요?**
A: 기본적으로 마인크래프트에 존재하는 모든 아이템을 판매 목록에 추가할 수 있습니다. 다만, 아이템 ID를 정확히 입력해야 하며, 아이템명은 마인크래프트의 내부 ID 규칙을 따라야 합니다(예: "minecraft:apple"). 커스텀 아이템의 경우 해당 아이템의 정확한 네임스페이스와 ID를 알아야 합니다.

**Q: 에메랄드 외에 다른 화폐로 변경할 수 있나요?**
A: 네, 코드를 수정하여 다른 아이템을 화폐로 사용하도록 변경할 수 있습니다. 코드에서 에메랄드 검사 부분과 차감 부분을 원하는 아이템으로 변경하면 됩니다. 또한 복수의 화폐 시스템을 구현하거나, 스코어보드를 활용한 가상 화폐를 도입하는 것도 가능합니다.

**Q: 이 상점 시스템이 서버 성능에 미치는 영향은 어떤가요?**
A: 이 UI 상점 시스템은 비교적 가벼운 편으로, 일반적인 서버 환경에서 큰 성능 저하 없이 작동합니다. 다만 매우 많은 플레이어가 동시에 상점을 이용하거나, 상점 아이템 목록이 지나치게 많은 경우에는 약간의 부하가 발생할 수 있습니다. 대규모 서버에서는 아이템 목록을 적절히 분류하여 여러 상점으로 나누는 것이 좋습니다.

## 추가 리소스

- [GitHub 소스 코드](https://github.com/ssakspirit/scriptAPI/blob/main/UIStore.js)
- [스크립트 API 시작하기 튜토리얼](https://youtu.be/zBVdaQ0AXOY)
- [마인크래프트 베드락 에디션 스크립트 API 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/)
- [스티브 코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)
- [베드락 에디션 UI API 공식 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/minecraft/server/ui)

## 이런 분들에게 추천합니다

- 마인크래프트 서버 운영자 및 관리자
- 커스텀 게임 시스템을 만들고 싶은 월드 제작자
- 스크립트 API와 UI 개발에 관심 있는 개발자
- 서버 내 경제 시스템을 구축하려는 커뮤니티 운영자
- 마인크래프트 애드온 제작에 도전하고 싶은 크리에이터
- 게임플레이 편의성을 높이는 기능을 찾는 서버 플레이어

## 관련 튜토리얼

- [스크립트 API로 본격적으로 애드온 제작하기](https://youtu.be/zBVdaQ0AXOY)
- [스크립트 API의 첫걸음, 채팅명령어 만들기](https://youtu.be/xb9Ke_HShU0)
- [사용자 인터페이스(UI) 제작하기](https://youtu.be/RnO28hLVPVo)
- [복붙한 코드를 애드온으로 바꾸기](https://youtu.be/lZuJxdKgUMg)
- [애드온 제작을 한다면 꼭 필요한 몇 가지!](https://youtu.be/7AZUk_p9LkQ)

## 실습 코드

```javascript
// UI 상점 시스템 (UIStore.js)
import { world, ItemStack, system } from "@minecraft/server";
import { ActionFormData, ModalFormData } from "@minecraft/server-ui";

// 상점에 판매할 아이템 정의
const storeItems = [
  "minecraft:golden_apple",
  "minecraft:potato",
  "minecraft:carrot",
  "minecraft:apple" // 영상에서 추가한 아이템
];

// 각 아이템의 가격 설정 (에메랄드 기준)
const itemPrices = {
  "minecraft:golden_apple": 3,
  "minecraft:potato": 2,
  "minecraft:carrot": 1,
  "minecraft:apple": 1 // 영상에서 추가한 아이템
};

// 아이템 이름 설정 (UI 표시용)
const itemNames = {
  "minecraft:golden_apple": "황금 사과",
  "minecraft:potato": "감자",
  "minecraft:carrot": "당근",
  "minecraft:apple": "사과" // 영상에서 추가한 아이템
};

// 나침반 우클릭 이벤트 리스너
world.beforeEvents.itemUse.subscribe(event => {
  const player = event.source;
  const item = event.itemStack;
  
  // 나침반 아이템인지 확인
  if (item.typeId === "minecraft:compass") {
    // 상점 UI 표시
    showStoreUI(player);
  }
});

// 상점 UI 표시 함수
function showStoreUI(player) {
  const storeForm = new ActionFormData()
    .title("UI 상점")
    .body("구매할 아이템을 선택하세요")
  
  // 모든 상점 아이템을 UI에 추가
  for (const item of storeItems) {
    storeForm.button(
      `${itemNames[item]} (${itemPrices[item]} 에메랄드)`
    );
  }
  
  // UI 표시하고 결과 처리
  storeForm.show(player).then(response => {
    if (response.canceled) return;
    
    // 선택한 아이템 인덱스
    const selectedItemIndex = response.selection;
    const selectedItem = storeItems[selectedItemIndex];
    
    // 수량 선택 UI 표시
    showQuantitySelector(player, selectedItem);
  });
}

// 수량 선택 UI 표시 함수
function showQuantitySelector(player, itemId) {
  const quantityForm = new ModalFormData()
    .title(`${itemNames[itemId]} 구매`)
    .slider("구매 수량", 1, 64, 1, 1);
  
  quantityForm.show(player).then(response => {
    if (response.canceled) return;
    
    // 선택한 수량
    const quantity = response.formValues[0];
    // 총 가격 계산
    const totalPrice = itemPrices[itemId] * quantity;
    
    // 아이템 구매 처리
    purchaseItem(player, itemId, quantity, totalPrice);
  });
}

// 아이템 구매 처리 함수
function purchaseItem(player, itemId, quantity, totalPrice) {
  // 인벤토리에서 에메랄드 확인
  let emeralds = 0;
  const inventory = player.getComponent("inventory");
  
  // 모든 인벤토리 슬롯 확인
  for (let i = 0; i < inventory.size; i++) {
    const item = inventory.getItem(i);
    if (item && item.typeId === "minecraft:emerald") {
      emeralds += item.amount;
    }
  }
  
  // 에메랄드가 충분한지 확인
  if (emeralds < totalPrice) {
    player.sendMessage(`§c에메랄드가 부족합니다. 필요: ${totalPrice}, 보유: ${emeralds}`);
    return;
  }
  
  // 에메랄드 차감 및 아이템 지급
  try {
    // 아이템 지급
    player.runCommand(`give @s ${itemId} ${quantity}`);
    // 메시지 전송
    player.sendMessage(`§a${itemNames[itemId]} ${quantity}개를 구매했습니다.`);
    // 에메랄드 차감
    player.runCommand(`clear @s minecraft:emerald ${totalPrice}`);
  } catch (error) {
    player.sendMessage(`§c구매 처리 중 오류가 발생했습니다: ${error}`);
  }
}
```

## 태그
#마인크래프트 #UI상점 #스크립트API #애드온제작 #베드락에디션 #게임개발 #커스텀상점 #서버관리 #에메랄드통화 #마인크래프트경제
