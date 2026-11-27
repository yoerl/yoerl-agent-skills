---
name: evidence-brief
description: >-
  One-page UX evidence brief for stakeholder meetings: issue, NNG pros/cons links,
  product context, recommendation. Use for design debate, "왜 이렇게", UX 설득,
  review meeting, heuristic tradeoff justification.
---

# UX Evidence Brief

회의·리뷰에서 **"NNG 링크만"이 아니라 결정 가능한 1페이지**를 만든다.

**선행:** 쟁점 1문장 (예: "모바일 햄버거 메뉴 유지 vs 전면 노출").  
**도구:** `nngroup` 스킬로 `site:nngroup.com` 검색·fetch.

## 절차

1. **쟁점** — 우리가 결정해야 할 1문장.
2. **옵션 A / B** (또는 현재안 vs 대안) 명시.
3. `nngroup` — 각 옵션·쟁점에 맞는 NNG 2~3건 (찬성·반대 모두).
4. **우리 맥락** — 도메인, 사용자, 화면 제약, 로그/테스트 있으면 인용.
5. **권고** — 1개 + 조건 ("~하면 A, 아니면 B").
6. **needs-test** — 데이터 없으면 다음 검증 1줄.

## 출력 (1페이지)

```markdown
## UX Evidence Brief — {쟁점}

**결정 필요:** …
**권고:** … (조건: …)

### 쟁점
…

### NNG 근거
| 관점 | 아티클 | 핵심 |
|------|--------|------|

### 우리 맥락
…

### 트레이드오프
| | 옵션 A | 옵션 B |
|---|--------|--------|

### 다음 단계
- [ ] …
```

## 주의

- NNG는 보편 원칙; **예외 정당화는 사용자 연구**.
- 링크 던지기만 하지 말고 **표로 비교**.
- 휴리스틱 번호 태그 (#6 등) 사용.