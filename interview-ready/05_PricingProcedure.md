# SAP MM Pricing Procedure – Interview Version

## 1. Pricing Procedure 개요

구매 문서에서 가격이 어떻게 계산되는지를 정의하는 규칙 집합.

기본 구조:

Condition Technique 기반

- Condition Type
- Access Sequence
- Pricing Procedure
- Condition Record

---

## 2. 가격 결정 흐름

PO 생성  
→ Pricing Procedure 결정  
→ Access Sequence 실행  
→ Condition Record 조회  
→ Condition Type 순서대로 계산

→ 최종 금액 결정

---

## 3. 주요 Condition Type 예시

PB00  
- 기본 가격

RA01  
- 할인

FRA1  
- 운임

세금 조건 등 추가 가능

---

## 4. Pricing Procedure 구성 요소

Step  
- 계산 순서

Condition Type  
- 가격 요소

Subtotal  
- 중간 합계 저장

Calculation Type  
- 금액/비율 계산 방식

---

## 5. Pricing Procedure 결정 기준

다음 조합으로 결정됨:

- Purchasing Organization
- Vendor Schema Group
- Document Schema Group

→ Schema Determination

---

## 6. 실무 오류 사례

가격이 0원

원인:
- Info Record 없음
- Condition Record 없음
- Access Sequence 불일치

가격 중복 계산

원인:
- Step 순서 오류
- Condition Type 중복

---

## 7. 면접용 40초 답변

"MM 가격결정은 Condition Technique 기반입니다.
PO 생성 시 Pricing Procedure가 결정되고,
Access Sequence를 통해 Condition Record를 찾습니다.
Condition Type들이 Step 순서에 따라 적용되며
PB00, 할인, 운임 등이 계산되어 최종 가격이 결정됩니다."