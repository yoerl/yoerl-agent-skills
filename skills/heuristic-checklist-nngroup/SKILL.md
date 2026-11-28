---
name: heuristic-checklist-nngroup
description: >-
  NN/G Jakob Nielsen 10 휴리스틱 정본 + 44항 체크리스트로 UI 전문가 휴리스틱
  분석. heuristic-checklist-nngroup, 닐슨 44항, NNG 10 heuristics, 사용성
  점검표, m4a_ic 체크리스트, 스크린샷·프로토타입 점검.
---

# Heuristic Checklist — NN/G 10 + 44항

**휴리스틱 분석(전문가 검토):** [NN/G 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) 정본 정의·팁과 **44개 세부 질문**으로 화면·플로우·앱 UI를 점검한다.  
**사용자 테스트 대체 불가** — 확인 못 한 항목은 `확인 못 함`으로 남긴다.

| 참고 | 용도 |
|------|------|
| [references/nngroup-ten-heuristics.md](references/nngroup-ten-heuristics.md) | **NN/G 정본** — 정의·예시·팁·관련 글 링크 |
| [references/checklist-44.md](references/checklist-44.md) | 44항 질문 (**문구 변경 금지**) |

**빠른 게이트:** `quick-scan` · **NNG 검색:** `nngroup`

## 선행

범위가 없으면 **Product / 대표 화면·플로우 / Device** 중 하나만 질문.

## 절차

1. 범위의 화면을 탐색한다. 스크린샷·URL·컴포넌트명을 메모한다.
2. 평가할 휴리스틱(#)마다 `references/nngroup-ten-heuristics.md`에서 **정의·팁**을 확인한다.
3. `references/checklist-44.md`의 **1.1 → 10.4** 순으로 각 질문에 판정을 붙인다.
4. 판정이 `아니오` 또는 `부분`이면 근거(화면 위치·요소) + 관련 NNG 원칙 한 줄 + 짧은 개선안.
5. 휴리스틱(#)별 미충족 수 집계 → 상위 5개 우선 (과업 막힘 > 반복 부담 > 다듬기).

## 판정 기준

| 판정 | 의미 |
|------|------|
| 예 | 근거와 함께 충족 |
| 부분 | 일부 화면·상태만 충족 또는 약한 충족 |
| 아니오 | 명확히 미충족 |
| 해당 없음 | 범위 밖 (예: 검색 없는 화면의 5.3) |
| 확인 못 함 | 자료·접근으로 검증 불가 |

**9.3 (사운드):** 웹·무음 환경이면 `해당 없음` + 비고. 모바일·네이티브는 확인.

## 출력 형식

```markdown
## 휴리스틱 체크리스트 — {Product} / {범위} / {Device}

### 요약
- 예: n/44 | 부분: n | 아니오: n | 해당 없음: n | 확인 못 함: n
- 미충족 상위: 1.3, 4.1, …

### 체크리스트

| ID | 판정 | 근거·비고 (NNG #) |
|----|------|-------------------|
| 1.1 | 예 | … |
| … | … | … |

### 휴리스틱별 미충족
| # | NN/G 이름 | 아니오+부분 |
|---|-----------|-------------|
| 1 | Visibility of System Status | … |

### 우선 개선 (최대 5)
1. **{ID}** — NNG #n … — 권장: …

### 다음
[ ] handoff-pack 전달 / [ ] 사용성 테스트
```

## 연계

| 스킬 | 용도 |
|------|------|
| `nngroup` | 최신 NNG 아티클·근거 검색 |
| `quick-scan` | 소규모 변경 얕은 검사 |
| `handoff-pack` | 개발·QA 전달 |
| `ux-review-dossier` | UXD 통합 기록 |