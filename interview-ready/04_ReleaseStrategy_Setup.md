# SAP MM Release Strategy – Interview Version

## 1. Release Strategy 개요

구매 문서(PR/PO)의 승인 프로세스를
조건 기반으로 제어하는 설정.

금액, 구매조직, 문서유형 등을 기준으로
승인 단계 자동 결정.

---

## 2. Classic Release Strategy 구조

설정 구성 요소:

1) Release Group  
2) Release Code (승인자)  
3) Release Indicator (상태)  
4) Release Strategy  
5) Classification (조건 연결)

---

## 3. 동작 흐름

PO 생성  
→ Classification 조건 평가  
→ 해당 Strategy 결정  
→ Release Code 순서대로 승인  
→ 승인 완료 후 후속 문서 가능

---

## 4. 예시 시나리오

조건:
- 금액 ≤ 10,000 → 자동 승인
- 10,000 ~ 50,000 → 1단계 승인
- > 50,000 → 2단계 승인

핵심:
Classification에서 금액 조건으로 전략 결정

---

## 5. 실무에서 자주 발생하는 오류

- Classification 특성 값 누락
- 승인자 권한 미매핑
- Changeability Indicator 설정 오류
- 승인 후 가격 변경 시 재승인 미적용

---

## 6. S/4HANA 차이

ECC:
- Classic Release Strategy 사용

S/4HANA:
- Flexible Workflow 권장
- BRF+ 기반 조건 설정

---

## 7. 면접용 40초 답변

"Release Strategy는 Classification 기반으로
금액이나 조직 조건에 따라 승인 단계를 자동 결정합니다.
Release Group, Code, Indicator, Strategy를 정의하고
특성 값을 통해 전략을 연결합니다.
S/4HANA에서는 Flexible Workflow로 확장되어
보다 유연한 승인 구성이 가능합니다."
