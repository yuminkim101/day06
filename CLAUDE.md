# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 이 폴더는 무엇인가

원티드 커리어캠프 6일차(D6) 수업 자료 폴더다. 빌드·린트·테스트 도구가 없다. 화면은 모두 **HTML 파일 하나(CSS·JS 포함)** 이고, 브라우저에서 더블클릭해 열어 확인한다. git 저장소가 아니다.

- `D06_1021.html`: 수업 워크북 문서(읽기용). 직접 고칠 대상이 아니다.
- `d6-api/`: 실습 결과물. 키 없이 쓰는 공개 API(Open-Meteo 등)를 `fetch`로 불러 보여 주는 화면을 둔다. 지금은 `weather.html`(현재 기온·날씨 코드를 말과 이모지로 변환).

## 규칙의 위치

API 화면 규칙은 `.claude/rules/api.md`에 있다(키 금지, `const API` 한 곳 + `// 🔌` 주석, "이 화면이 쓰는 API" 상자, 카드별 로딩·실패 화면, 출처·기준 날짜 표기, 커밋은 제안만). 규칙을 여기에 복사하지 말고 그 파일을 고친다. AI가 실수하면 같은 파일 맨 아래 `## 실수에서 배운 규칙`에 한 줄씩 추가한다.

## 검사

`/api-check <파일>`(`.claude/skills/api-check/SKILL.md`)은 HTML이 위 규칙을 지켰는지 표로 보고만 하고 고치지 않는다. 이 스킬은 `CLAUDE.md`를 기준으로 읽도록 쓰여 있는데, 규칙 본문은 `.claude/rules/api.md`에 있다. 검사 기준이 비어 보이면 그 파일을 읽는다.

## 화면을 만들 때 알아둘 것

- 날씨 코드는 WMO 숫자라서 `weather.html`의 `WEATHER` 표로 말·이모지로 바꾼다. 표에 없는 코드는 "알 수 없음"으로 보인다.
- 동네를 바꾸려면 `API`의 `latitude`/`longitude`와 화면 이름 `PLACE`를 함께 바꾼다.
