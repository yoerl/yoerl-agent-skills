---
name: ux-review-dossier
description: >-
  Write a UX Review Dossier (UXD, UX 통합 리뷰서) — one file combining nngroup,
  quick-scan, heuristic-evaluation, evidence-brief, handoff-pack. Use for UXD,
  "도스리에", 통합 리뷰서, ux dossier template.
---

# UX 통합 리뷰서 (UXD)

**UX Review Dossier** — 한 화면·한 시점에 UX 근거·스캔·평가·결정·handoff를 **한 파일**에 모은 문서.

| 한글 | 영문 | 약칭 |
|------|------|------|
| UX 통합 리뷰서 | UX Review Dossier | **UXD** |

**SSOT:** [references/template.md](references/template.md) · [references/verdict-rubric.md](references/verdict-rubric.md)

**예시:** `leeds_profile_next/docs/ux/dossiers/signup-2026-11-28.md`

## 트리거

- 출시·릴리즈 전 UX 점검 기록
- 여러 UX 스킬 결과를 **한 권**으로 묶을 때
- knowledge `ux-knowledge/reviews/` 등록

## 선행

Product / Task / Device / User Group (없으면 Task 하나만 질문).

## 작성 절차

1. §0 메타 + 판정 ([verdict-rubric](references/verdict-rubric.md))
2. §1 요약 — 판정·심각도·액션 3개
3. §2 `nngroup` — NNG 2~3건 + 맥락
4. §3 `quick-scan` — 5H 표 + 판정
5. §4 `heuristic-evaluation` — 이슈 표 (또는 보류 건)
6. §5 `evidence-brief` — 쟁점 있을 때만
7. §6 `handoff-pack` — 개발·QA·기획
8. §7 후속·wiki·재스캔

## 경로 규칙

| 위치 | 패턴 |
|------|------|
| 제품 레포 | `docs/ux/dossiers/{task-slug}-{YYYY-MM-DD}.md` |
| knowledge wiki | `wiki/ux-knowledge/reviews/{task-slug}-{YYYY-MM-DD}.md` |

## wiki 등록

지식 관리자 handoff → `ux-knowledge/reviews/` + raw 날짜 폴더.

## 연계 스킬

`nngroup` · `quick-scan` · `heuristic-evaluation` · `evidence-brief` · `handoff-pack`