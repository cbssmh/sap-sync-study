# SAP MM Pricing Procedure 심화 정리

## 1. Pricing Procedure란?
- 구매 문서에서 가격이 계산되는 전체 규칙 집합
- 어떤 조건을 어떤 순서로 적용할지 정의
- MM 가격결정의 최종 실행 로직

---

## 2. Pricing Procedure의 역할
- 기본가격, 할인, 운임, 세금 계산
- 총 금액 산출 방식 통제
- 회계 전기 금액의 기준 제공

---

## 3. Pricing Procedure 구성 요소

### Step
- 조건 적용 순서
- 숫자가 작을수록 먼저 계산

### Condition Type
- 가격 요소
- 예: PB00(기본가격), RA01(할인), FRA1(운임)

### Calculation Type
- 금액/비율/수량 기준 계산 방식

### Subtotal
- 중간 합계 저장
- 통계/후속 계산에 사용

---

## 4. Pricing Procedure 결정 기준
- Purchasing Organization
- Vendor Schema Group
- Document Schema Group

→ 세 조건의 조합으로 하나의 Pricing Procedure 결정

---

## 5. 가격결정 흐름 (실무)
1) PO 생성
2) Pricing Procedure 결정
3) Access Sequence 실행
4) Condition Record 검색
5) Step 순서대로 가격 계산
6) 최종 금액 확정

---

## 6. 실무 포인트
- 가격 안 맞으면 Pricing Procedure부터 확인
- Step 순서 오류로 금액 중복 계산 사례 존재
- 신규 Condition 추가 시 영향 범위 테스트 필수
- 컨설턴트는 “이 가격이 어떻게 계산됐는지” 설명 가능해야 함