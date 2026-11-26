---
name: test-case
description: >-
  Write detailed test cases (TC-*) with a fixed 10-section format — sequence
  diagrams, steps, expected results; no Pass/Fail until execution. Use when
  the user asks to create or expand detailed test cases, TC documents, or
  to unfold targets from a scenario document's "상세 TC 대상" section. Also
  triggers on "테스트케이스 작성", "상세 TC", "TC 문서", "test-case".
---

# Detailed Test Case Authoring

프로젝트의 테스트케이스를 **상세 TC** 형식으로 작성한다.  
양식 SSOT: [references/template-detailed.md](references/template-detailed.md) (10절 고정).

## test-scenario 스킬과의 연동

1. **시나리오 선행:** 기능 흐름을 먼저 정리하려면 `test-scenario` 스킬로 `docs/test-case/*_SCENARIO.md`를 만든다.
2. **펼칠 대상:** 시나리오 문서의 `## 상세 TC 대상` 표에 적힌 예약 `TC-*` ID·범위부터 본문을 작성한다.
3. **매핑 유지:** 각 TC의 `시나리오 원본` 칸에 해당 `TS-*` ID와 시나리오 파일 경로를 남긴다.

시나리오 없이 단일 TC만 요청받아도 동일 양식을 따른다.

## 핵심 원칙

- 실행 전에는 범위와 문서 구조를 먼저 정리한 뒤 작성한다.
- 한 화면 안에서는 권한, 상태, 검증, 모달, 토스트, 배너, 리다이렉트 분기를 모두 케이스로 쪼갠다.
- 권한 분기가 있으면 같은 화면이라도 합치지 말고 각각 독립 TC로 작성한다.
- 결과물은 `docs/test-case/{YYYYMMDD_HHMMSS}/{BUSINESS_DOMAIN}/{SCREEN_NAME}/{FEATURE}_TESTCASE.md` 구조를 따른다.
- 생성이 끝나면 각 파일의 제목과 TC ID를 모아 `docs/test-case/{YYYYMMDD_HHMMSS}/INDEX.md` 형태의 인덱스 문서를 함께 만든다.
- **판정·실제 결과는 비운다.** 에이전트가 채우지 않는다.
- **테스트 실행 금지.** 문서 작성만 한다.

## TC 내용 순서 (10절, 고정)

1. 기본 식별 및 관리 정보
2. 사전 조건
3. 테스트 입력 데이터
4. 시퀀스 다이어그램
5. 시퀀스 다이어그램 기준 흐름
6. 검증 로직
7. 테스트 수행 절차
8. 예상 결과
9. 실제 결과 및 판정 (비움)
10. 참조 API

절을 합치거나 빼지 않는다. 자세한 칸 설명·예시는 [template-detailed.md](references/template-detailed.md)를 따른다.

## 실행 순서

0. 같은 흐름의 `docs/test-case/*_SCENARIO.md`가 있으면 연다. `## 상세 TC 대상`의 예약 `TC-*`·범위를 이번 작성 scope로 삼는다.
1. 라우트, 컴포넌트, 문서, API 흐름을 훑어 대상 화면·분기를 확정한다.
2. 각 `TC-*`에 10절 골격을 채운다.
3. 화면별로 권한·상태 분기가 있으면 별도 TC로 분리한다.
4. 필요하면 여러 파일로 나눠 저장하고 인덱스 문서를 만든다.
5. 마지막에 `판정`·`실제 결과` 칸이 비었는지, ID 중복이 없는지 점검한다.

## 출력 기준

- 저장 경로와 TC ID·제목 목록을 사용자에게 알려준다.
- 함께 생성한 인덱스 문서 경로도 알려준다.
- 문서는 에디터에서 깨지지 않도록 표, `---`, 코드블록, Mermaid를 연속 과밀하게 배치하지 말고, TC 사이에는 빈 줄을 둔다.
- `Test Steps`는 표 셀 안에 `<br>`로 넣지 말고 별도 섹션·번호 목록·실제 줄바꿈만 사용한다.

## 시퀀스·흐름 규칙

- 각 TC는 `시퀀스 다이어그램`을 먼저 두고, 그 아래에 `시퀀스 다이어그램 기준 흐름표`를 배치한다.
- participant 이름은 `화면`이 아니라 `로그인 화면`, `장바구니 화면`처럼 실제 화면명·라우트 의미가 드러나게 쓴다.
- `시퀀스 다이어그램 기준 흐름표`와 `테스트 수행 절차`는 같은 내용을 반복하지 않는다.

## 하지 말 것

- 다른 목차(체크리스트, 성공/실패만 있는 표)로 바꿔 쓰지 않는다
- 9번 판정을 에이전트가 채우지 않는다
- 시퀀스 다이어그램 칸을 빼거나, 이 TC와 무관한 전체 시스템 그림을 넣지 않는다
- `docs/test-case/{YYYYMMDD_HHMMSS}/{BUSINESS_DOMAIN}/{SCREEN_NAME}/` 밖에 테스트케이스를 저장하지 않는다