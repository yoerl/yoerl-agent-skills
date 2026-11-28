# yoerl-agent-skills

회사·CulWonder 하네스와 **독립**인 에이전트 스킬 모음. 테스트 시나리오·상세 TC·시나리오 풀 문서·시맨틱 HTML 워크플로를 [Cursor Skills](https://cursor.com/docs/agent/skills) 형식으로 제공한다.

## 설치

```sh
# 스킬별 설치
npx skills add yoerl/yoerl-agent-skills@test-scenario -y
npx skills add yoerl/yoerl-agent-skills@test-case -y
npx skills add yoerl/yoerl-agent-skills@test-scenario-full -y
npx skills add yoerl/yoerl-agent-skills@semantic-html -y
npx skills add yoerl/yoerl-agent-skills@heuristic-evaluation -y
npx skills add yoerl/yoerl-agent-skills@nngroup -y
npx skills add yoerl/yoerl-agent-skills@quick-scan -y
npx skills add yoerl/yoerl-agent-skills@evidence-brief -y
npx skills add yoerl/yoerl-agent-skills@handoff-pack -y
npx skills add yoerl/yoerl-agent-skills@ux-review-dossier -y
npx skills add yoerl/yoerl-agent-skills@heuristic-checklist-nngroup -y
```

## 스킬 목록

| 스킬 | 설명 |
|------|------|
| **test-scenario** | `TS-*`당 파일 1개 — `TS→TC` 트리·케이스 표. 실행·판정·하위 TS 없음 |
| **test-case** | 10개 항목 고정 양식의 상세 TC. 시나리오 **케이스 표**의 `TC-*` ID와 연동 |
| **test-scenario-full** | **시나리오 1개 = md 파일 1개.** 그 파일에 시나리오 정보 + 케이스 요약표 + **모든 TC 상세**(목적·유형·우선순위·전제·입력·절차·기대 결과·실행 결과 칸). 단독 설치 가능 |
| **semantic-html** | WHATWG HTML 카탈로그 + tiered 절차 (A/B/C 참조)로 시맨틱 마크업·리팩터링 |
| **heuristic-evaluation** | Jakob Nielsen 10 휴리스틱 전체 평가 — 2-pass, 이슈 표, 심각도, needs-test |
| **heuristic-checklist-nngroup** | NN/G 10휴리스틱 정본 + **44항** 체크리스트 + 한국어 가이드 — 전문가 점검
| **nngroup** | nngroup.com `site:` 검색 + 아티클 fetch·요약·맥락 검증 |
| **quick-scan** | PR·작은 변경용 5휴리스틱 얕은 스캔 — 통과/보류/풀평가 (에이전트 시간 강제 없음) |
| **evidence-brief** | 회의용 UX 근거 1페이지 — 쟁점, NNG 찬반, 권고 |
| **handoff-pack** | 평가 결과를 화면개발·QA·기획 handoff 문구로 분해 |
| **ux-review-dossier** | **UX 통합 리뷰서 (UXD)** — 5스킬 결과 + 판정 기준을 한 md에 통합 |

### UX 스킬 파이프라인

```
quick-scan → (보류) → heuristic-checklist-nngroup 또는 heuristic-evaluation → handoff-pack
                ↘ evidence-brief (회의·논쟁 시)
nngroup (어디서든 근거 검색)
        ↘ ux-review-dossier (UXD 통합 기록)
```

**UXD** = UX Review Dossier (UX 통합 리뷰서). 판정: `ux-review-dossier/references/verdict-rubric.md`

NNG·휴리스틱 정본 wiki: `knowledge/wiki/ux-knowledge/` (오너 knowledge 레포, 선택).

## harness_culwonder와의 관계

동일 워크플로가 [harness_culwonder](https://github.com/yoerl/harness_culwonder)에 **CulWonder 전용으로 래핑**되어 있다:

| 이 레포 (일반) | harness_culwonder (CulWonder) |
|----------------|-------------------------------|
| `test-scenario` 스킬 | `/culwonder-test-scenario <흐름>` 명령 |
| `test-case` 스킬 | `/culwonder-test-case-create-all` 명령 |
| `semantic-html` 스킬 | `skills/semantic-html/` (동일 WHATWG v2 본문) |

하네스는 CulWonder init·wiki·agent-safety 룰과 번들되어 제품 레포에 배포한다. 이 레포는 **어떤 프로젝트에도** `npx skills add`로 직접 설치할 수 있다.

## 출처·라이선스

MIT License — see [LICENSE](LICENSE).

**Attribution**

- `heuristic-checklist-nngroup`: NN/G [10 heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) + m4a_ic 44항 체크리스트
- `test-scenario` · `test-case`: harness_culwonder `skills/culwonder/references/` 시나리오·TC 워크플로에서 일반화
- `semantic-html`: harness_culwonder `skills/semantic-html/` (SKILL.md, references/*, evals)에서 복사 (MIT)