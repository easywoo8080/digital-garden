---
title: text write guide
draft: false
tags:
---

# Cheat Sheet
| 기호 | 의미 | 사용 예시 |
| --- | --- | --- |
| **`< >`** | **필수 입력 변수** (사용자가 직접 값을 채워 넣어야 하는 항목) | `git clone <repository_url>` |
| **`[ ]`** | **선택 입력 항목** (필요할 때만 추가하는 생략 가능한 옵션) | `docker run [-d] [--name <container_name>] <image>` |
| **`{ }`** | **필수 선택 그룹** (제시된 집합 중 하나를 반드시 선택) | `git checkout {-b |
| **`|`** | **상호 배타적 구분 (OR)** (여러 옵션 중 하나만 선택) | `npm run {dev | build | start}` |
| **`...`** | **반복 입력 가능** (동일 형태의 인자를 여러 개 연속 입력) | `mkdir <directory_name1> [directory_name2 ...]` |
| **`_`** | **기본값 (Default)** (별도 지정 없을 때 자동 적용되는 값) | `PORT=[<u>8080</u>|3000]` |



---

### 1. POSIX 표준 (IEEE Std 1003.1)

명령줄 도구의 인자 및 옵션 표기법에 대한 가장 근본적인 국제 표준입니다.

* **문서명:** *IEEE Std 1003.1 / POSIX Utility Conventions (Section 12.1 Utility Argument Syntax)*
* **주요 내용:**
* 대괄호 `[ ]`는 생략 가능한 옵션(Optional)을 의미합니다.
* 꺾쇠괄호 `< >` 또는 이탈릭체는 사용자가 실제로 채워 넣어야 하는 필수 인자(Argument/Operand)를 의미합니다.



---

### 2. 마이크로소프트 기술 문서 스타일 가이드 (Microsoft Style Guide)

소프트웨어 및 개발자 문서 작성 시 사용하는 세계적인 표준 가이드라인입니다.

* **문서명:** *Microsoft Style Guide - Command Syntax Conventions*
* **표준 표기 규칙:**
* **`< >` (Angle brackets):** 사용자가 지정해야 하는 매개변수/필수 항목 (예: `<file_name>`)
* **`[ ]` (Brackets):** 선택 항목/옵션 (예: `[--help]`)
* **`{ }` (Braces):** 서로 배타적인 필수 선택 항목 집합 중 하나 선택 (예: `{a | b | c}`)
* **`|` (Vertical bar):** 상호 배타적인 옵션 구분을 의미



---

### 3. ISO/IEC 14977 (EBNF 표준)

프로그래밍 언어나 구문 분석을 정의할 때 사용하는 국제 표준 문법 표기법(Extended Backus-Naur Form)입니다.

* **문서명:** *ISO/IEC 14977: Information technology — Syntactic metalanguage — Extended BNF*
* **주요 내용:**
* `[ ... ]` 또는 `/? ... ?/`: 생략 가능한 영역 (Option)
* `{ ... }`: 0회 이상 반복 가능한 영역 (Repetition)
* `( ... )`: 그룹화 (Grouping)



---

### 4. 리눅스 맨 페이지 표기 규칙 (man page)

리눅스/유닉스 계열 시스템 명령어 매뉴얼 작성 시 따르는 공식 가이드입니다.

* **문서명:** *man-pages(7) - conventions for writing Linux man pages*
* **주요 내용:**
* `bold`: 입력할 문자 그대로의 키워드/명령어
* *italic* 또는 `< >`: 사용자 지정 변수/필수 인자
* `[ ]`: 선택 사항(Options)



---

### 대표적인 표기법 요약표

| 기호 | 의미 | 예시 |
| --- | --- | --- |
| **`< >`** | **필수 입력 매개변수** (Placeholder/Required) | `git push <remote> <branch>` |
| **`[ ]`** | **선택 입력 항목** (Optional) | `ls [-l] [-a]` |
| **`{ }`** | **선택 집합 또는 필수 그룹** (Choice/Group) | `chmod {+ |
| **`|`** | **택일 / OR 연산자** (Exclusive OR) | `[yes |

참고할 수 있는 공식 문서를 직접 확인하고 싶으시다면 **Microsoft Style Guide의 Command Syntax Conventions** 항목이나 리눅스의 **`man 7 man-pages`** 문서를 검색해 보시는 것을 추천합니다.