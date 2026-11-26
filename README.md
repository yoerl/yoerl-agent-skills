# yoerl-agent-skills

회사·CulWonder 하네스와 **독립**인 에이전트 스킬 모음. 테스트 시나리오·상세 TC·시맨틱 HTML 워크플로를 [Cursor Skills](https://cursor.com/docs/agent/skills) 형식으로 제공한다.

## 설치

```sh
# 스킬별 설치
npx skills add yoerl/yoerl-agent-skills@test-scenario -y
npx skills add yoerl/yoerl-agent-skills@test-case -y
npx skills add yoerl/yoerl-agent-skills@semantic-html -y
```

## 스킬 목록

| 스킬 | 설명 |
|------|------|
| **test-scenario** | `TS-*`당 파일 1개 — `TS→TC` 트리·케이스 표. 실행·판정·하위 TS 없음 |
| **test-case** | 10절 고정 양식의 상세 TC. 시나리오 **케이스 표**의 `TC-*` ID와 연동 |
| **semantic-html** | WHATWG HTML 카탈로그 + tiered 절차 (A/B/C 참조)로 시맨틱 마크업·리팩터링 |

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

- `test-scenario` · `test-case`: harness_culwonder `skills/culwonder/references/` 시나리오·TC 워크플로에서 일반화
- `semantic-html`: harness_culwonder `skills/semantic-html/` (SKILL.md, references/*, evals)에서 복사 (MIT)