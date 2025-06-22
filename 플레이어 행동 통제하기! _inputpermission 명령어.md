---
title: "플레이어 행동 통제하기! /inputpermission 명령어"
date: "2025-04-25"
thumbnail: "https://i.ytimg.com/vi/Imn0wk6ByiU/hqdefault.jpg"
tags: ["명령어", "베드락", "에듀케이션", "롱폼"]
url: "https://www.youtube.com/watch?v=Imn0wk6ByiU"
duration: "3:30"
series: "마인크래프트 명령어 튜토리얼"
difficulty: "중급"
---

# 플레이어 행동 통제하기! /inputpermission 명령어

<div align="center">
<img src="https://i.ytimg.com/vi/Imn0wk6ByiU/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 베드락 에디션과 에듀케이션 에디션에서 사용 가능한 `/inputpermission` 명령어를 소개합니다. 이 명령어를 사용하면 특정 조건에 따라 플레이어의 다양한 행동(점프, 이동, 카메라 조작 등)을 제어할 수 있습니다. 예제로 다이아몬드를 들고 있을 때 점프를 제한하는 시스템을 구현하는 방법을 상세히 보여줍니다. 교육용 환경이나 커스텀 게임 제작에 유용한 기능입니다.

## 주요 내용

### 1. inputpermission 명령어 소개
- 플레이어의 행동을 제어하는 명령어 기능 설명
- 제어 가능한 다양한 행동 목록 (점프, 이동, 카메라 등)
- 명령어 기본 구문 및 사용법

### 2. 태그 시스템을 활용한 조건부 제어
- 특정 아이템 소지 여부에 따른 태그 부여
- 태그 기반 조건부 명령 실행
- 태그 초기화 및 상태 업데이트 메커니즘

### 3. 커맨드 블록 체인 설계
- 반복형 및 체인형 커맨드 블록 활용
- 명령어 실행 순서 및 흐름 설계
- 무조건부 실행과 조건부 실행의 차이

## 실습 과정

1. **기능 시연 (00:00-00:30)**
   - 다이아몬드를 들고 있을 때 점프 불가능 시연
   - 다이아몬드를 버리면 점프 가능해짐
   - 게임 모드와 상관없이 작동하는 것 확인

2. **커맨드 블록 설정 확인 (00:30-01:30)**
   - 4개의 커맨드 블록 구성 살펴보기
   - 첫 번째 블록: 다이아몬드 소지 플레이어에게 태그 부여
   - 두 번째 블록: 태그 있는 플레이어 점프 비활성화
   - 세 번째 블록: 태그 없는 플레이어 점프 활성화
   - 네 번째 블록: 태그 초기화

3. **명령어 상세 분석 (01:30-02:30)**
   - inputpermission 명령어 구문 설명
   - query 옵션으로 현재 권한 상태 확인하기
   - set 옵션으로 권한 설정하기
   - 다양한 행동 제어 옵션 살펴보기

4. **다양한 적용 예시 (02:30-끝)**
   - 카메라 제어 예시 시연
   - 교육용 에디션에서의 활용 방안
   - 커스텀 게임 제작에 활용하는 방법

## 자주 묻는 질문

**Q: inputpermission 명령어로 제어할 수 있는 모든 행동은 무엇인가요?**  
A: 주요 제어 가능한 행동으로는 점프(jump), 카메라 이동(camera), 전체 이동(movement), 앞/뒤/좌/우 이동(forward, back, left, right), 웅크리기(sneak), 탈것 관련 동작(mount, dismount) 등이 있습니다. 명령어를 입력할 때 탭 키를 누르면 사용 가능한 모든 옵션을 확인할 수 있습니다.

**Q: 명령어에서 @s는 무엇을 의미하나요?**  
A: @s는 현재 명령어를 실행하는 주체를 가리킵니다. execute 명령어와 함께 사용될 경우, execute as @a[tag=has_diamond]에서 @s는 has_diamond 태그를 가진 각 플레이어를 의미합니다.

**Q: 태그를 초기화하는 이유는 무엇인가요?**  
A: 태그를 초기화해야 플레이어가 아이템을 버리거나 새로 획득했을 때 즉시 상태를 업데이트할 수 있습니다. 초기화하지 않으면 한번 태그가 부여된 상태가 계속 유지되어, 실제 아이템 소지 상태와 맞지 않게 됩니다.

**Q: 자바 에디션에서도 이 명령어를 사용할 수 있나요?**  
A: 아니요, inputpermission 명령어는 베드락 에디션과 에듀케이션 에디션에서만 사용 가능합니다. 자바 에디션에서는 이와 동일한 기능을 구현하기 위해 다른 방식의 명령어나 데이터팩을 사용해야 합니다.

## 추가 리소스

- [마인크래프트 베드락 명령어 공식 문서](https://learn.microsoft.com/ko-kr/minecraft/creator/documents/commandsintroduction)
- [마인크래프트 에듀케이션 에디션 공식 웹사이트](https://education.minecraft.net/)
- [태그 시스템 활용 가이드](https://minecraft.fandom.com/wiki/Commands/tag)
- [커맨드 블록 체인 설계 튜토리얼](https://www.youtube.com/link-to-command-block-tutorial)

## 이런 분들에게 추천합니다

- 마인크래프트에서 커스텀 미니게임을 제작하고 싶은 개발자
- 교육용 에디션으로 학습 환경을 구성하는 교사
- 플레이어 행동 제어가 필요한 어드벤처 맵 제작자
- 명령어 시스템을 심도 있게 배우고 싶은 중급 플레이어
- 조건부 메커니즘을 구현하고 싶은 레드스톤 엔지니어

## 관련 튜토리얼

- 태그 시스템으로 플레이어 관리하기
- 커맨드 블록 체인 설계 방법
- 교육용 에디션에서 학습 환경 구성하기
- execute 명령어 활용 심화
- 조건부 명령 실행 시스템 설계

## 커맨드 블록 설정

```
# 첫 번째 커맨드 블록 (반복형, 항상 활성)
/tag @a[hasitem={item=diamond,quantity=1..}] add has_diamond

# 두 번째 커맨드 블록 (체인형, 무조건, 항상 활성)
/execute as @a[tag=has_diamond] run inputpermission set @s jump disabled

# 세 번째 커맨드 블록 (체인형, 무조건, 항상 활성)
/execute as @a[tag=!has_diamond] run inputpermission set @s jump enabled

# 네 번째 커맨드 블록 (반복형, 무조건, 항상 활성)
/tag @a remove has_diamond
```

## 다양한 inputpermission 명령어 예시

```
# 현재 권한 상태 확인
/inputpermission query @s jump disabled
/inputpermission query @s camera enabled

# 다양한 행동 제어
/inputpermission set @s movement disabled  # 모든 이동 제한
/inputpermission set @s camera disabled    # 카메라 회전 제한
/inputpermission set @s forward disabled   # 앞으로 이동 제한
/inputpermission set @s sneak disabled     # 웅크리기 제한
/inputpermission set @s mount disabled     # 탈 것 타기 제한
/inputpermission set @s dismount disabled  # 탈 것 내리기 제한

# 모든 행동 한번에 제어
/inputpermission set @s * disabled         # 모든 행동 제한
/inputpermission set @s * enabled          # 모든 행동 허용
```

## 태그
#마인크래프트 #베드락 #에듀케이션 #명령어 #inputpermission #플레이어제어 #커맨드블록 #태그시스템 #게임제작 #조건부실행
