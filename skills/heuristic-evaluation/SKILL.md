---
name: heuristic-evaluation
description: >-
  Full Jakob Nielsen 10-heuristic evaluation of a UI flow: scope, 2-pass review,
  issue table, severity, needs-test tags. Use for heuristic evaluation, UX review
  workbook, usability inspection, "10 heuristics", "휴리스틱 평가", "워크북".
---

# Heuristic Evaluation

Jakob Nielsen **10 usability heuristics**로 화면·플로우·프로토타입을 평가한다.  
**사용자 리서치 대체 불가** — 보편 원칙 + 맥락 검증 1문장 필수.

**선행:** 범위가 없으면 **Product / Task / User Group / Device** 중 하나만 질문.  
**후행:** 팀 전달은 `handoff-pack` 스킬. 빠른 PR 게이트는 `quick-scan` 스킬.

**참고:** [references/ten-heuristics.md](references/ten-heuristics.md)  
**원문:** [10 heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) · [How to conduct](https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/)

## 절차

### 1. 준비

- 범위: **한 Task · 한 Device** (첫 평가·대형 제품).
- 다인: **3~5인 독립 평가** → 서로 결과 보기 전 → 통합.
- 기록: Issues / Recommendations (워크북 형식).

### 2. 평가 (사람 1~2h; 에이전트는 깊이 우선·시간 강제 없음)

1. **1회차** — 태스크만 수행, 평가 없음.
2. **2회차** — 10 휴리스틱 위반 탐색 (`references/ten-heuristics.md`).
3. 이슈마다 **#번호**, 화면·요소명.
4. **위반 ≠ 무조건 수정** — 트레이드오프 1줄 (예: 모바일 햄버거 vs #6).

### 3. 통합 (다인)

- affinity 클러스터
- 심각도: **Critical / Major / Minor**
- **`needs-test`**: 사용자 연구로 검증 필요

### 4. QA 역할 구분

| 휴리스틱 평가 | 기능 QA |
|---------------|---------|
| 설계 품질 (정성) | TC·시나리오 실행 |

## 출력 형식

```markdown
## 휴리스틱 평가 — {Product} / {Task} / {Device}

### 요약
Critical: n | Major: n | Minor: n | needs-test: …

### 이슈

| # | 휴리스틱 | 이슈 | 권장 | 심각도 | 비고 |
|---|----------|------|------|--------|------|

### 맥락 검증
…

### 다음 단계
[ ] 수정 / [ ] 사용성 테스트 / [ ] 기획
```

## 연계

| 스킬 | 용도 |
|------|------|
| `quick-scan` | PR·작은 변경 얕은 게이트 |
| `nngroup` | NNG 아티클 근거 |
| `evidence-brief` | 회의 설득 1페이지 |
| `handoff-pack` | 화면개발·QA·기획 분리 전달 |