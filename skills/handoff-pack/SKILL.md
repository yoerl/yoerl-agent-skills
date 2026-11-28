---
name: handoff-pack
description: >-
  Split heuristic evaluation or UX review results into handoff messages for
  frontend dev, QA tester, and product/planning roles. Use after evaluation,
  "팀에 넘겨줘", "handoff", 개발·QA·기획 전달.
---

# Handoff Pack

휴리스틱 평가·리뷰 결과를 **역할별 실행 문구**로 분해한다. 평가 표 1개 → 받는 쪽 3~4종.

**선행:** 이슈 목록 또는 `heuristic-checklist-nngroup` / `quick-scan` 출력.

## 분류 규칙

| 수신 | 포함 이슈 |
|------|-----------|
| **화면 개발** | UI·컴포넌트·상호작용·피드백·#1 #5 #6 #8 #9 시각·동작 수정 |
| **QA** | `needs-test`, #5·#9 검증 시나리오, 회귀 범위 |
| **기획** | #2 용어·카피, #4 일관성·정책, #10 도움말 |
| **지식** (선택) | wiki 등록용 요약 — 요청 시만 |

## 절차

1. 각 이슈에 **#휴리스틱**, **심각도**, **화면/요소** 확인.
2. 위 표로 **한 이슈는 한 역할** (중복 시 주 역할 1개 + CC 1줄).
3. 역할별 **액션 동사** 권장안: "변경", "검증", "정책 확정".
4. 화면 개발 handoff: 파일/컴포넌트 추정 가능하면 명시 (코드 있을 때).

## 출력

```markdown
## Handoff Pack — {Product} / {Task}

### → 화면 개발
- [#9 Major] … → **권장:** …

### → QA
- [needs-test] … → **시나리오:** Given … When … Then …

### → 기획
- [#2] … → **카피/정책:** …

### 스킵 (의도적 위반·보류)
- …
```

## Orca 봇 (선택)

오너 환경에 handoff 보낼 때:

```text
orchestration send --to bot:화면 개발자 --type handoff --subject "…" --body "…"
orchestration send --to bot:QA 테스터 --type handoff …
orchestration send --to bot:기획자 --type handoff …
```

**보내기 전** 오너 확인 — 자동 전송 기본값 아님.

## 주의

- 평가 표를 그대로 복붙하지 않는다 — **역할별 액션만**.
- QA는 TC 실행이 아니라 **범위·시나리오 제안** (실행은 QA 봇).