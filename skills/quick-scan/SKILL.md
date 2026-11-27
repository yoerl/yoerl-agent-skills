---
name: quick-scan
description: >-
  Shallow UX gate: scan only heuristics #1 #5 #9 #6 #2 on a small UI change;
  output pass/hold/full-eval verdict. No time limit for agents. Use for PR UX
  review, quick heuristic check, "게이트", "빠른 UX 리뷰", merge before UX pass.
---

# Quick Scan (Heuristic Gate)

**10개 전부 아님** — 치명도 높은 **5개만** 스캔하고 **통과 / 보류 / 풀평가** 판정.  
에이전트는 **시간 강제 없음** (가능한 빨리; 범위·출력만 고정).

**선행:** 범위 없으면 Product·Task·Device 중 하나만 질문.  
**후행:** 보류 → `handoff-pack` 또는 `heuristic-evaluation`. 근거 회의 → `evidence-brief`.

## 스캔 순서 (고정)

| # | 휴리스틱 | 본다 |
|---|----------|------|
| 1 | 상태·피드백 | 로딩, 저장/제출 결과, 비동기 상태 |
| 5 | 오류 방지 | 위험 행동 확인, 실수 유발 UI |
| 9 | 오류·복구 | 메시지 plain language, 해결책 |
| 6 | 인식·정보 | 숨은 필수 정보, 네비 discoverability |
| 2 | 용어 | 내부 jargon, 사용자 모르는 라벨 |

**하지 않음:** #3~#4·#7~#8·#10 전체 (보류 시 풀평가로).

## 절차

1. 범위 1줄 (Product / Task / Device).
2. 입력 검토: diff, 스크린샷, URL, 설명.
3. 위 5휴리스틱만 — **Critical / Major** 만 기록 (Minor 생략 가능).
4. 판정:

| 판정 | 조건 |
|------|------|
| **통과** | Critical 0, Major 0~1 경미 |
| **보류** | Critical≥1 또는 Major 다수 |
| **풀평가** | 영향·논쟁 큼, 범위 불명확 |

## 출력 (짧게)

```markdown
## Quick Scan — {Product} / {Task} / {Device}

**판정:** 통과 | 보류 | 풀평가

| 휴리스틱 | 이슈 | 심각도 |
|----------|------|--------|

**한 줄:** …
**다음:** …
```

## 주의

- 감 코멘트 금지 — **#번호 + 심각도**.
- 위반 ≠ 반드시 수정 (1줄 트레이드오프).
- 브라우저 검증 필요하면 명시; 없으면 텍스트·스크린 기준.