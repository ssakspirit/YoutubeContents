---
title: "사용자 인터페이스(UI)제작하기 #애드온제작"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/q6igVaSz0-8/hqdefault.jpg"
tags: ["중급", "베드락", "스크립트API", "소스코드", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=q6igVaSz0-8"
duration: "3:56"
series: "애드온제작"
episode: ""
difficulty: "중급"
---

# 사용자 인터페이스(UI)제작하기 #애드온제작

<div align="center">
<img src="https://i.ytimg.com/vi/q6igVaSz0-8/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션의 스크립트 API를 활용하여 사용자 인터페이스(UI)를 제작하는 방법을 설명합니다. 나침반 아이템을 오른쪽 클릭하면 UI 창이 나타나고, 위치 저장 및 이동 기능을 구현하는 과정을 단계별로 보여줍니다. 이 튜토리얼은 스크립트 API를 활용한 UI 제작의 기본 개념을 이해하는 데 도움이 됩니다.

## 주요 내용

### 1. UI 기본 구성 요소 이해
- 액션 폼 데이터를 활용한 UI 창 생성
- 제목(타이틀), 설명(바디) 및 버튼 구현
- 이벤트 리스너를 통한 버튼 클릭 감지

### 2. 위치 저장 및 이동 시스템 구현
- 플레이어 현재 위치 좌표 저장 메커니즘
- 저장된 위치로 텔레포트 기능 구현
- 저장된 위치가 없을 때 오류 메시지 표시

### 3. 아이템 사용 이벤트 처리
- 특정 아이템(나침반) 사용 시 UI 창 열기
- 아이템 ID 확인 및 이벤트 처리 방법
- 명령어 실행을 통한 메시지 표시

## 실습 과정

1. **UI 기능 시연 (00:00-01:00)**
   - 나침반을 오른쪽 클릭하여 UI 창 열기
   - 위치 저장 및 이동 기능 시연
   - 위치 저장 없이 이동 시도 시 오류 메시지 확인

2. **코드 구조 이해 (01:01-02:15)**
   - 액션 폼 데이터 불러오기
   - 플레이어 위치 좌표 변수 선언
   - 아이템 사용 이벤트 감지 및 처리

3. **UI 제작 및 버튼 구현 (02:16-03:10)**
   - UI 창 제목 및 설명 설정
   - 저장하기와 이동하기 버튼 생성
   - 버튼 클릭 이벤트 처리 로직 구현

4. **기능 구현 완성 (03:11-끝)**
   - 위치 저장 기능 구현 (변수에 좌표 저장)
   - 저장된 위치로 이동 기능 구현 (텔레포트 명령어 실행)
   - 저장된 위치가 없을 때 오류 메시지 표시 로직

## 자주 묻는 질문

**Q: 스크립트 API를 사용하기 위한 사전 준비는 무엇인가요?**  
A: 스크립트 API를 사용하기 위해서는 먼저 마인크래프트 베드락 에디션이 필요하며, 애드온 개발을 위한 기본적인 자바스크립트 지식이 필요합니다. 또한 영상에서 언급된 스크립트 API 시작하기 튜토리얼을 참고하는 것이 좋습니다.

**Q: UI 창을 다른 아이템에도 적용할 수 있나요?**  
A: 네, 코드에서 아이템 ID 체크 부분을 수정하여 다른 아이템에도 쉽게 적용할 수 있습니다. 영상에서는 나침반(compass)을 사용했지만, 원하는 아이템의 ID로 변경하면 됩니다.

**Q: UI 창에 더 많은 버튼이나 기능을 추가할 수 있나요?**  
A: 네, 액션 폼 데이터 내에 더 많은 버튼을 추가할 수 있으며, 각 버튼에 대한 이벤트 처리 로직을 구현하면 다양한 기능을 추가할 수 있습니다. switch 문 내에 더 많은 case를 추가하여 각 버튼마다 다른 기능을 구현할 수 있습니다.

**Q: 저장된 위치 데이터는 게임을 종료하면 유지되나요?**  
A: 영상에서 구현한 방식은 게임 세션 내에서만 위치 데이터가 유지됩니다. 게임을 종료하면 데이터가 소실됩니다. 데이터를 영구적으로 저장하려면 데이터베이스나 파일 시스템을 활용하는 방법을 고려해야 합니다.

## 추가 리소스
- [스크립트 API 시작하기](https://youtu.be/zBVdaQ0AXOY)
- [코드 복붙하기 (GitHub)](https://github.com/ssakspirit/scriptAPI/blob/main/UItp.js)
- [베드락 공식 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/scriptapi/minecraft/server/minecraft-server)
- [브릿지 가이드](https://youtu.be/L2s8-w8HXIk?si=aWJONVaLN0kngFtg)
- [스티브코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)

## 이런 분들에게 추천합니다
- 마인크래프트 베드락 에디션에서 커스텀 UI를 개발하고 싶은 개발자
- 스크립트 API를 활용한 애드온 제작에 관심 있는 중급 이상 사용자
- 게임 내 사용자 경험을 향상시키는 인터페이스를 만들고 싶은 크리에이터
- 자바스크립트를 활용한 게임 개발에 관심 있는 프로그래머
- 마인크래프트에 텔레포트 기능 등 유용한 기능을 추가하고 싶은 서버 운영자

## 관련 튜토리얼
- [스크립트 API 시작하기 #애드온제작]
- [채팅명령어 만들기 #애드온제작]
- [본격적으로 애드온 제작하기 #애드온제작]
- [말이 많은 NPC 만들기 #애드온제작튜토리얼]
- [채팅창에 시간을 쓰면 동작하는 타이머 시작! #애드온제작]

## 실습 코드
```javascript
import { ActionFormData } from "@minecraft/server-ui";

// 플레이어 위치 좌표 변수 선언
let playerPositionX = null;
let playerPositionY = null;
let playerPositionZ = null;

// 아이템 사용 이벤트 리스너
world.events.itemUse.subscribe((data) => {
    // 아이템 ID 확인 (나침반인 경우)
    if (data.itemStack.typeId === "minecraft:compass") {
        // 플레이어 정보 저장
        const player = data.source;
        // UI 폼 함수 호출
        showTeleportForm(player);
    }
});

// UI 폼 생성 및 표시 함수
function showTeleportForm(player) {
    // 액션 폼 데이터 생성
    const formData = new ActionFormData();
    
    // UI 제목과 설명 설정
    formData.title("순간 이동 장치");
    formData.body("위치를 저장하거나 저장된 위치로 이동합니다.");
    
    // 버튼 추가
    formData.button("위치 저장하기");
    formData.button("저장된 위치로 이동하기");
    
    // 폼 표시 및 결과 처리
    formData.show(player).then(response => {
        // 폼이 닫히거나 취소된 경우
        if (response.canceled) return;
        
        // 버튼 클릭 처리
        switch (response.selection) {
            // 첫 번째 버튼 (위치 저장)
            case 0:
                // 현재 위치 저장
                playerPositionX = player.location.x;
                playerPositionY = player.location.y;
                playerPositionZ = player.location.z;
                
                // 메시지 표시
                player.runCommand("title @s actionbar 위치 저장 완료");
                break;
                
            // 두 번째 버튼 (위치 이동)
            case 1:
                // 저장된 위치가 없는 경우
                if (playerPositionX === null) {
                    player.runCommand("title @s actionbar 저장된 장소가 없습니다.");
                }
                // 저장된 위치가 있는 경우
                else {
                    // 저장된 위치로 텔레포트
                    player.runCommand(`tp @s ${playerPositionX} ${playerPositionY} ${playerPositionZ}`);
                    player.runCommand("title @s actionbar 이동 완료");
                }
                break;
        }
    });
}
```

## 태그
#마인크래프트 #베드락에디션 #스크립트API #UI제작 #사용자인터페이스 #애드온 #자바스크립트 #텔레포트
