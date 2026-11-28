---
name: nngroup
description: >-
  Search and summarize Nielsen Norman Group (nngroup.com): site search, article
  fetch, UX evidence with context check. Use for NNG, Nielsen Norman, design
  rationale, usability articles, "nngroup에서 찾아줘", UX 근거.
---

# Nielsen Norman Group

NNG 아티클·가이드를 **검색·읽기·요약**한다. 감이 아닌 **근거(제목+URL)** 를 남긴다.

**검색 절차 SSOT:** [references/search.md](references/search.md)  
**연계:** 평가 `heuristic-checklist-nngroup` · 설득 `evidence-brief`

## 트리거

- 설계·리서치 **근거** 필요
- `nngroup.com` 검색·요약
- 휴리스틱·패턴·방법론 질문

## 절차

1. 질문 → **영문 키워드** (`references/search.md` 주제표).
2. `WebSearch` → `site:nngroup.com <키워드>`.
3. 관련 1~2건 `WebFetch` 본문 읽기.
4. 요약에 포함:
   - NNG 원칙 (제목+링크)
   - **우리 제품·사용자 맥락** 1문장
   - 필요 시 자사 테스트·로그 검증 제안
5. 무료 아티클·영상 우선; 유료 리포트는 언급만.

## 출력

```markdown
### NNG 근거
- **[제목](URL)** — bullet 2~4
- **우리 맥락**: …
- **관련 검색**: …
```

## 주의

- 한국어 질문 → 영문 검색 → 한국어 요약.
- NNG는 보편 원칙; 도메인은 별도 검증.