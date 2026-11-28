# 10 Usability Heuristics (NN/G 정본)

**원문:** [10 Usability Heuristics for User Interface Design](https://www.nngroup.com/articles/ten-usability-heuristics/) (Jakob Nielsen, 1994 · NNG 최종 검토 2024-01-30)

휴리스틱은 **구체적 가이드라인이 아니라 넓은 경험 규칙(rules of thumb)** 이다. 1994년 이래 10원칙 자체는 유지되었고, 2020·2024 갱신에서 설명·예시·팁이 보강되었다.

**역사:** Molich & Nielsen (1990) 휴리스틱 평가 → Nielsen (1994) 249개 사용성 문제 요인 분석으로 본 세트 확정.

**인용:** Jakob Nielsen, nngroup.com/articles/ten-usability-heuristics 또는 Nielsen (1994a).

44항 체크리스트 ID 매핑은 각 절의 **체크** 줄을 따른다.

---

## 1. Visibility of System Status

**정의:** 합리적 시간 내 적절한 피드백으로 사용자에게 무슨 일이 일어나고 있는지 알려야 한다.

**의미:** 현재 상태를 알면 이전 상호작용 결과를 학습하고 다음 단계를 정한다. 예측 가능한 상호작용은 제품·브랜드 신뢰를 만든다.

**예시:** 쇼핑몰 지도의 “You Are Here” — 현재 위치로 다음 이동을 이해하게 한다.

**팁 (NN/G)**

- 사용자에게 결과가 있는 행동은 상태를 알리지 않고 실행하지 않는다.
- 피드백은 가능한 한 빠르게(이상적으로 즉시) 준다.
- 열린·지속적 소통으로 신뢰를 쌓는다.

**관련:** [Visibility of System Status](https://www.nngroup.com/articles/visibility-system-status/) · **체크:** 1.1–1.5

---

## 2. Match Between the System and the Real World

**정의:** 사용자 언어를 써야 한다. 내부 전문용어 대신 사용자에게 익숙한 단어·구문·개념을, 자연스럽고 논리적인 순서로 보여준다.

**의미:** 동료에게는 분명해 보이는 용어·아이콘·이미지가 사용자에게는 낯설 수 있다. 실세계 관례·자연적 매핑(natural mapping)이면 학습·기억이 쉽고 직관적으로 느껴진다.

**예시:** 전기레인지 조작부가 가열판 배치와 일치하면 어느 다이얼이 어디를 제어하는지 바로 안다.

**팁 (NN/G)**

- 정의를 찾아보지 않고도 의미를 이해할 수 있게 한다.
- 자신과 사용자의 언어·개념 이해가 같다고 가정하지 않는다.
- 리서치로 사용자 익숙 용어·멘털 모델을 파악한다.

**관련:** [Match Between the System and the Real World](https://www.nngroup.com/articles/match-system-real-world/) · **체크:** 2.1–2.5

---

## 3. User Control and Freedom

**정의:** 사용자는 실수를 자주 한다. 긴 과정 없이 원치 않는 행동에서 빠져나갈 **명확한 비상구**가 필요하다.

**의미:** 쉬운 뒤로가기·실행 취소는 자유·자신감을 준다. 탈출 경로가 있으면 막혀 좌절하지 않고 시스템을 계속 제어한다.

**예시:** 물리 공간처럼 디지털에도 빠른 비상 탈출이 필요하다.

**팁 (NN/G)**

- Undo / Redo를 지원한다.
- Cancel 등 현재 상호작용을 끝내는 명확한 출구를 둔다.
- 출구는 잘 보이고 발견 가능하게 라벨한다.

**관련:** [User Control and Freedom](https://www.nngroup.com/articles/user-control-and-freedom/) · **체크:** 3.1–3.5

---

## 4. Consistency and Standards

**정의:** 다른 단어·상황·행동이 같은 뜻인지 헷갈리지 않게 한다. 플랫폼·업계 관례를 따른다.

**의미:** Jakob's Law — 사용자는 다른 제품에 더 많은 시간을 쓴다. 그 경험이 기대를 만든다. 일관성이 깨지면 새로 배워야 해 **인지 부하**가 는다.

**예시:** 호텔 체크인 카운터는 보통 로비 앞 — 기대에 부합한다.

**팁 (NN/G)**

- **내부 일관성:** 한 제품·제품군 안에서 통일.
- **외부 일관성:** 업계·플랫폼 관례 준수.
- 두 종류 모두 학습성을 높인다.

**관련:** [Consistency and Standards](https://www.nngroup.com/articles/consistency-and-standards/) · **체크:** 4.1–4.6

---

## 5. Error Prevention

**정의:** 좋은 오류 메시지도 중요하지만, 최선은 문제가 생기기 **전에** 막는 것이다. 오류 유발 조건을 없애거나, 실행 전 확인 옵션을 준다.

**의미:** 오류는 **Slip**(부주의·무의식)과 **Mistake**(의도적이나 멘털 모델 불일치)로 나뉜다.

**예시:** 산길 가드레일 — 클리프 추락을 예방한다.

**팁 (NN/G)**

- 고비용 오류부터 예방·낮은 좌절은 그다음.
- Slip — 제약·좋은 기본값.
- Mistake — 기억 부담 줄이기, undo, 경고.

**관련:** [Preventing User Errors](https://www.nngroup.com/articles/slips/) · **체크:** 5.1–5.4

---

## 6. Recognition Rather than Recall

**정의:** 요소·행동·옵션을 **보이게** 해 기억 부담을 최소화한다. 인터페이스 한쪽 정보를 다른 쪽에서 기억하지 않아도 된다. 필드 라벨·메뉴 항목 등은 필요할 때 보이거나 쉽게 찾을 수 있어야 한다.

**의미:** 단기 기억은 한계가 있다. 인식(recognition)을 돕는 UI는 인지 노력을 줄인다.

**예시:** “포르투갈 수도는?” 보다 “리스본이 포르투갈 수도인가?”가 더 잘 맞춘다.

**팁 (NN/G)**

- 기억하게 하지 말고 화면에서 인식하게 한다.
- 긴 튜토리얼 대신 맥락 도움을 준다.
- 사용자가 기억해야 할 정보 양을 줄인다.

**관련:** [Recognition vs. Recall](https://www.nngroup.com/articles/recognition-and-recall/) · **체크:** 6.1–6.4

---

## 7. Flexibility and Efficiency of Use

**정의:** 초보자에게는 숨기고, 숙련자에게는 단축·가속을 제공해 **초보·숙련 모두** 만족시킨다. 자주 쓰는 동작은 맞춤 설정 가능하게 한다.

**의미:** 프로세스를 여러 방식으로 수행할 수 있게 하면 사용자가 맞는 방법을 고를 수 있다.

**예시:** 지도의 일반 경로 vs 현지인의 지름길.

**팁 (NN/G)**

- 키보드 단축키·제스처 등 가속기.
- 개인화 — 사용자별 콘텐츠·기능.
- 사용자 설정으로 동작 방식 선택.

**관련:** [Flexibility and Efficiency](https://www.nngroup.com/articles/flexibility-efficiency/) · **체크:** 7.1–7.4

---

## 8. Aesthetic and Minimalist Design

**정의:** 관련 없거나 거의 쓰이지 않는 정보는 넣지 않는다. UI의 **추가 정보 단위**마다 핵심 정보와 경쟁해 상대적 가시성이 떨어진다.

**의미:** 플랫 디자인 강제가 아니라 **핵심에 집중** — 시각 요소가 사용자 주목표를 지원해야 한다.

**예시:** 장식 과한 주전자 — 손잡이·세척 난이도처럼 장식이 사용성을 해칠 수 있다.

**팁 (NN/G)**

- 콘텐츠·시각을 필수에 맞춘다.
- 불필요 요소가 필요한 정보를 빼앗지 않게 한다.
- 주목표를 지원하도록 우선순위를 둔다.

**관련:** [Aesthetic and Minimalist Design](https://www.nngroup.com/articles/ten-usability-heuristics/#toc-8-aesthetic-and-minimalist-design) · **체크:** 8.1–8.5

---

## 9. Help Users Recognize, Diagnose, and Recover from Errors

**정의:** 오류 메시지는 일상 언어(오류 코드 남발 금지), 문제를 정확히 짚고, 건설적으로 해결책을 제시한다. 사용자가 **알아차리고 인식**할 수 있는 시각 처리도 필요하다.

**예시:** 일방통행 반대방향 표지 — 잘못된 방향을 알리고 멈추게 한다.

**팁 (NN/G)**

- 굵은 빨간 텍스트 등 익숙한 오류 시각 언어.
- 기술 전문용어 없이 무엇이 잘못됐는지 설명.
- 오류를 바로 풀 수 있는 단축·해결책 제공.

**관련:** [Error-Message Guidelines](https://www.nngroup.com/articles/error-message-guidelines/) · **체크:** 9.1–9.4

---

## 10. Help and Documentation

**정의:** 이상적으로는 추가 설명 없이 과제를 완료할 수 있어야 한다. 필요하면 문서로 도움을 준다.

**의미:** 도움말·문서는 **검색하기 쉽고**, 사용자 **과제에 초점**을 맞추며, 간결하고 **구체적 단계**를 나열해야 한다.

**예시:** 공항 안내 키오스크 — 맥락에서 즉시 문제를 푼다.

**팁 (NN/G)**

- 도움말 검색이 쉬워야 한다.
- 가능하면 필요한 순간 맥락에 바로 제시.
- 수행할 구체 단계를 나열.

**관련:** [Help and Documentation](https://www.nngroup.com/articles/help-and-documentation/) · **체크:** 10.1–10.4

---

## 평가 시 활용

- 44항 질문 판정 전 해당 번호(#) 절의 **정의·팁**을 읽고 맥락에 맞게 적용한다.
- `부분`·`아니오` 근거에 어느 NNG 원칙(정의/팁)에 걸렸는지 짧게 적을 수 있다.
- 더 깊은 최신 근거가 필요하면 `nngroup` 스킬로 원문·관련 아티클을 검색한다.