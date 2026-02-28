# SAP MM–FI Integration (Journal Entry Focus)

## 1. 핵심 개념

MM은 수량을 관리하고,  
FI는 금액을 관리한다.

두 모듈은 Movement Type + OBYC를 통해 자동으로 연결된다.

---

## 2. 기본 회계 흐름

### ① PO 생성
- 회계 전표 없음
- 약정 단계

---

### ② GR (Movement Type 101)

예: 수량 100, 단가 10,000

회계 분개:

Dr. Inventory (BSX)
Cr. GR/IR (WRX)

→ 재고 증가 + GR/IR 부채 발생

---

### ③ IR (Invoice Receipt)

송장 금액 일치 시:

Dr. GR/IR
Cr. Vendor (AP)

→ GR/IR 상계
→ 실제 매입채무 확정

---

### ④ Payment

Dr. Vendor
Cr. Cash/Bank

→ 지급 완료

---

## 3. 가격 차이 발생 시

### Standard Price 사용 시

실제 구매가 > 표준가

Dr. Inventory (표준가)
Dr. Price Difference (PRD)
Cr. GR/IR

→ 가격 차이는 PRD 계정으로 분리

---

### Moving Average Price 사용 시

- 가격차이 계정 없음
- 재고 금액이 직접 조정됨

---

## 4. 출고(261 예시)

Dr. Cost (GBB)
Cr. Inventory (BSX)

→ 재고 감소 + 비용 인식

---

## 5. OBYC 구조 요약

Movement Type
→ Transaction Key (BSX / WRX / GBB / PRD)
→ Valuation Class
→ G/L Account
→ FI Document 생성

---

## 6. 실무 오류 분석 포인트

- 재고는 정상인데 금액이 틀림
  → Price Control 확인

- GR/IR 잔액 남음
  → GR/IR 상계 여부 점검

- 출고 시 잘못된 비용 계정
  → GBB 매핑 확인

---

## 7. 면접용 40초 답변 구조

"MM과 FI는 Movement Type 기반 자동 계정결정으로 연결됩니다.
GR 시 재고와 GR/IR이 발생하고,
IR 시 GR/IR이 Vendor로 상계됩니다.
Standard Price 사용 시 가격차이는 PRD로 분리됩니다.
이 모든 과정은 OBYC에서 Transaction Key와 Valuation Class 매핑을 통해 결정됩니다."