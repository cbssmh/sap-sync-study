# SAP MM 가격결정 (Condition Technique) 정리

## 1. Condition Technique란?
- 구매 가격을 결정하는 SAP 표준 메커니즘
- 가격, 할인, 세금, 운임 등을 조건(Condition)으로 관리
- MM 가격결정의 핵심 개념

---

## 2. 가격결정 적용 대상
- Purchase Order (PO)
- Purchasing Info Record
- 계약(Contract)

---

## 3. Condition Technique 구성 요소

### Condition Type
- 가격 요소의 종류
- 예: PB00(기본가격), RA01(할인), FRA1(운임)

### Condition Record
- 실제 가격 데이터
- 자재, 공급업체, 구매조직 기준으로 유지

### Access Sequence
- 어떤 순서로 조건을 찾을지 정의
- 자재+공급업체 → 자재 → 공급업체 순 등

### Pricing Procedure
- 가격 계산 순서와 로직 정의
- 어떤 Condition Type을 어떤 순서로 적용할지 결정

---

## 4. 가격결정 흐름
1) PO 생성
2) Pricing Procedure 호출
3) Access Sequence 따라 Condition Record 검색
4) Condition Type 적용
5) 최종 구매 가격 산출

---

## 5. 실무 포인트
- 가격 안 잡히는 문제의 대부분은 Condition Record 누락
- PB00 없으면 기본가격 미결정
- 구매조직/플랜트 기준 불일치 자주 발생
- 컨설턴트는 “어디서 가격이 결정되는지” 설명 가능해야 함
