---
title: Welcome to My Digital Garden
draft: false
tags:
  - welcome
  - home
---

문서의 전달력을 극대화하기 위해 "상단 핵심 요약(Advanced)"과 "하단 상세 본문 및 예제"의 2단계 구조로 구성된 마크다운 작성 및 독해 가이드입니다.

---

## 1. 마크다운 문서 작성 및 독해 가이드 (Quick Summary)

> **💡 핵심 요약 (Advanced)**
> * **목적:** 정보 소비 속도 최적화 — 바쁜 독자는 상단 요약만 읽고 판단하며, 상세 구현이나 설명이 필요한 경우 본문으로 이동합니다.
> * **문서 구조:**
> 1. **Advanced Summary Zone:** 접기/펼치기(`details`), 인용구(`>`), Highlight 카드 형식으로 작성.
> 2. **Detailed Body Zone:** 헤더(`##`, `###`), 비교 표, 코드 블록, 시각화 요소를 활용한 상세 설명.
> 
> 
> * **가독성 규칙:** 핵심 키워드는 **강조**, 본문 내 코드는 Inline Code(``code``)로 구분.
> 
> 

---

## 2. 상세 작성 가이드 및 독해 법 (Detailed Guide)

### Zone 1: 상단 어드밴스드 요약 작성법

상단 요약 영역은 독자가 **10초 이내에 전체 내용의 80%를 파악**할 수 있도록 구성합니다.

* **인용구(Blockquote) 및 강조:** `>` 기호를 활용해 시각적으로 본문과 분리합니다.
* **접기/펼치기 (`<details>`):** 요약 내용이 길어질 경우 접이식 영역을 사용해 화면 공간을 절약합니다.

#### 작성 예시:

```markdown
> ⚡ **Advanced Summary**
> * **핵심 개념:** API 요청 시 인증 헤더 필수 누락 방지
> * **적용 대상:** Backend API v2.0 이상
> * **주요 변경점:** Token 방식이 `Bearer`에서 `Custom HMAC`으로 변경됨
> 
> <details>
> <summary><b>🔍 3줄 요약 더보기</b></summary>
> 
> 1. 기존 Bearer 토큰 인증 방식은 2026년 12월 부로 Deprecated 됩니다.
> 2. 신규 API 요청은 `/api/v2/` 엔드포인트를 사용해야 합니다.
> 3. 상세 서명 생성 알고리즘은 하단 [인증 알고리즘 구현] 섹션을 참고하세요.
> </details>

```

---

### Zone 2: 하단 상세 본문 및 예제 작성법

본문은 논리적 흐름에 따라 구체적인 설명, 규격, 코드 예제, 시각적 비교 요소를 배치합니다.

#### 1) 구체적인 설명 및 비교 표

정보의 대비가 필요할 때는 마크다운 표(Table)를 사용합니다.

```markdown
### 변경 사항 비교

| 구분 | 기존 (v1.0) | 변경 (v2.0) | 비고 |
| :--- | :--- | :--- | :--- |
| **인증 방식** | Bearer Token | HMAC-SHA256 | 보안 강화 |
| **응답 속도** | ~120ms | ~45ms | 캐시 구조 개선 |

```

#### 2) 가독성 높은 코드 블록 및 예제

코드나 실습 예제는 언어명(Syntax Highlighting)을 지정하여 기술합니다.

```markdown
### 인증 알고리즘 구현 예시

`Authorization` 헤더에 들어갈 서명을 생성하는 Python 예제입니다.

```python
import hmac
import hashlib

def generate_signature(secret_key: str, message: str) -> str:
    return hmac.new(
        secret_key.encode('utf-8'),
        message.encode('utf-8'),
        hashlib.sha256
    ).hexdigest()

```

```

---

## 3. 문서를 보는 법 (독해 가이드)

이 템플릿으로 작성된 문서를 읽을 때는 아래 단계에 따라 읽으면 효율적입니다.

1. **1단계 (Overview):** 맨 위 `Advanced Summary` 박스만 빠르게 스캔하여 본인이 찾는 정보인지 확인합니다.
2. **2단계 (Deep Dive):** 필요한 경우 `<details>` 탭을 눌러 핵심 맥락을 파악합니다.
3. **3단계 (Implementation):** 하단 본문으로 이동하여 목차(TOC)나 헤더(`##`)를 따라 필요한 소스코드, 구체적인 파라미터, 예시를 참조합니다.

```