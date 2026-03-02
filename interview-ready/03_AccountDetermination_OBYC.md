# SAP MM Account Determination (OBYC) – Interview Version

## 1. OBYC의 역할

OBYC는 자재 이동 시 어떤 G/L 계정으로 전기할지를 결정하는 설정이다.

구조:

Movement Type  
→ Transaction Key  
→ Valuation Class  
→ G/L Account  
→ FI Document 생성

---

## 2. 기본 동작 흐름

예: Movement Type 101 (입고)

1) Movement Type 101 실행
2) Transaction Key = BSX / WRX 결정
3) 자재의 Valuation Class 확인
4) OBYC에서 해당 G/L 계정 매핑
5) 회계 전표 자동 생성

---

## 3. 주요 Transaction Key

### BSX – 재고 계정
- 입고 시 차변
- 출고 시 대변

### WRX – GR/IR 계정
- GR 시 대변
- IR 시 차변 상계

### GBB – 소비/출고 계정
- 261, 201 등 출고 처리

### PRD – 가격 차이
- Standard Price 사용 시 발생

---

## 4. Standard vs Moving Average 영향

Standard Price:
- 실제 구매가 ≠ 표준가 → PRD 계정 발생

Moving Average:
- 가격 차이 계정 없음
- 재고 금액 직접 변경

---

## 5. 실무에서 자주 발생하는 오류

- Valuation Class 미설정
- G/L 계정 미유지
- Chart of Accounts 불일치
- Movement Type 오해

---

## 6. 면접용 30초 답변

"계정결정은 OBYC에서 설정하며,
Movement Type에 따라 Transaction Key가 호출되고,
자재의 Valuation Class 기준으로 G/L 계정이 매핑됩니다.
예를 들어 101 입고 시 BSX와 WRX가 호출되고,
Standard Price 사용 시 PRD 계정이 추가로 발생합니다."
