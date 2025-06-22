---
title: "명령어 실행 금지! 교육용 에디션 월드의 비밀, education.json"
date: "2025-04-26"
thumbnail: "https://i.ytimg.com/vi/UpczQ675Da8/hqdefault.jpg"
tags: ["고급", "에듀케이션", "가이드", "설계자", "롱폼"]
url: "https://www.youtube.com/watch?v=UpczQ675Da8"
duration: "4:35"
series: "교육용 에디션 고급 설정"
episode: 1
difficulty: "고급"
---

# 명령어 실행 금지! 교육용 에디션 월드의 비밀, education.json

<div align="center">
<img src="https://i.ytimg.com/vi/UpczQ675Da8/hqdefault.jpg" alt="썸네일" width="600"/>
</div>

## 목차
- [소개](#소개)
- [주요 내용](#주요-내용)
- [실습 과정](#실습-과정)
- [자주 묻는 질문](#자주-묻는-질문)
- [추가 리소스](#추가-리소스)

## 소개
이 영상은 마인크래프트 교육용 에디션의 월드에서 명령어 실행을 제한하는 방법을 설명합니다. 학생들에게 교육용 월드를 제공할 때 특정 명령어를 비활성화하거나 모든 명령어를 차단하여 교육 목표에 집중할 수 있도록 돕는 education.json 파일의 역할과 수정 방법을 상세히 알려줍니다.

## 주요 내용

### 1. education.json 파일의 역할
- 교육용 에디션 월드에서 특정 기능 제한 가능
- 학생들이 허용된 활동만 할 수 있도록 제어
- 설정 내 치트 활성화 옵션과는 별개로 작동하는 강력한 제한 메커니즘

### 2. 명령어 제한 방법
- 모든 명령어 차단하기
- 특정 명령어만 선택적으로 차단하기
- 자동화 명령어(커맨드 블록, MC 함수) 차단하기

### 3. 응용 방법
- 교육 목적에 맞는 제한된 환경 구성하기
- 여러 월드에 동일한 설정 적용하기
- 특정 명령어만 허용하는 맞춤형 환경 구성하기

## 실습 과정

1. **education.json 파일 찾기 (00:00-01:20)**
   - 사용자 폴더 > AppData > Roaming > Minecraft Education Edition > games > com.mojang 경로 찾기
   - 최근 플레이한 월드 폴더 확인하기
   - education.json 파일 찾기
   - 텍스트 에디터(메모장, 워드패드 등)로 파일 열기

2. **파일 내용 분석 및 수정 (01:21-03:00)**
   - commandsHiddenFromPlayer 부분 확인하기
   - 별표(*) 기호의 의미 이해하기 (모든 명령어 차단)
   - 별표 제거하고 특정 명령어만 입력하기 (예: "give", "gamemode")
   - 파일 저장하고 월드 재시작하기

3. **설정 적용 확인 및 응용 (03:01-끝)**
   - 차단된 명령어와 허용된 명령어 테스트하기
   - 다른 월드에 education.json 파일 복사하여 적용하기
   - 코드 작성기 관련 설정 수정하기
   - commandsHiddenFromAutomation 설정 확인하기

## 자주 묻는 질문

**Q: education.json 파일이 없는 경우 어떻게 해야 하나요?**
A: 새로운 education.json 파일을 생성하여 월드 폴더에 추가할 수 있습니다. 영상에서 보여주는 내용을 참고하여 필요한 설정을 직접 작성하면 됩니다.

**Q: 베드락 에디션에서도 이 기능을 사용할 수 있나요?**
A: 아쉽게도 이 기능은 마인크래프트 교육용 에디션에서만 작동합니다. 베드락 에디션에서는 해당 기능을 사용할 수 없습니다.

**Q: 한번 제한한 명령어를 다시 활성화하려면 어떻게 해야 하나요?**
A: education.json 파일을 다시 열어 commandsHiddenFromPlayer 부분에서 해당 명령어를 제거하고 저장한 후 월드를 재시작하면 됩니다.

**Q: 일부 명령어만 제한하고 나머지는 허용하고 싶다면 어떻게 해야 하나요?**
A: commandsHiddenFromPlayer 설정에 제한하고 싶은 특정 명령어만 쉼표로 구분하여 나열하면 됩니다. 예: "give,gamemode,tp"

## 추가 리소스
- [마인크래프트 에듀케이션 공식 웹사이트](https://education.minecraft.net/)
- [마인크래프트 교육용 에디션 명령어 가이드](https://education.minecraft.net/ko-kr/resources/coordinate-and-commands)
- [교육용 에디션 설정 가이드](https://education.minecraft.net/ko-kr/resources/minecraft-education-edition-teacher-academy)
- [스티브코딩 페이스북 페이지](https://www.facebook.com/stvcoding/)

## 이런 분들에게 추천합니다
- 학생들을 위한 맞춤형 교육 환경을 구성하고 싶은 교사
- 교육용 월드를 설계하여 학생들에게 제공하는 교육자
- 교육용 에디션의 고급 설정을 배우고 싶은 사용자
- 학생들이 학습 목표에 집중할 수 있도록 게임 환경을 제한하고 싶은 관리자

## 관련 튜토리얼
- 메이크코드 튜토리얼 프로젝트 만들어 마인크래프트로 불러오기
- 교육용 에디션에서 클래스룸 모드 활용하기
- 교육용 에디션 세계 빌더 권한 설정하기
- 코드 작성기 기능 제한하기

## 실습 코드
```
[education.json 파일 기본 구조]
{
  "commandsHiddenFromPlayer": ["give", "gamemode"],
  "commandsHiddenFromAutomation": ["*"],
  "codeBuilderDefaultUri": "https://minecraft.makecode.com/..."
}

[모든 명령어 차단 설정]
"commandsHiddenFromPlayer": ["*"]

[특정 명령어만 차단 설정]
"commandsHiddenFromPlayer": ["give", "gamemode", "tp", "teleport"]

[자동화 명령어 차단 설정]
"commandsHiddenFromAutomation": ["*"]
```

## 태그
#마인크래프트 #에듀케이션 #교육용에디션 #명령어 #education.json #게임설정 #교육환경설정 #스티브코딩
