# SAP MM + FI 통합 흐름 (분개 레벨 설명)

## 1. 개요
- MM 물류 처리 시 FI 회계 전표 자동 생성
- 수량(Material Document)과 금액(Accounting Document)이 동시에 발생

---

## 2. PO 생성 단계
- 회계 전표 없음
- 구매 약정만 생성

---

## 3. GR (입고) 처리 – Movement Type 101

예:
- 수량 100개
- 단가 10,000
- 총액 1,000,000

### 회계 분개 (Standard Price 기준)

차변 (Debit)
- 재고자산 (BSX)

대변 (Credit)
- GR/IR (WRX)

분개 예:
Dr. Inventory        1,000,000
Cr. GR/IR            1,000,000

---

## 4. IR (송장 처리)

예:
- 송장 금액 1,000,000

차변
- GR/IR

대변
- 매입채무 (Vendor)

Dr. GR/IR            1,000,000
Cr. Vendor AP        1,000,000

→ GR/IR 계정 상계 완료

---

## 5. 가격 차이 발생 시 (Standard Price)

예:
- 표준가 10,000
- 실제 구매가 10,500

차변
- 재고자산 (표준가 기준)
- 가격차이(PRD)

대변
- GR/IR

Dr. Inventory        1,000,000
Dr. Price Diff       50,000
Cr. GR/IR            1,050,000

---

## 6. Moving Average Price 사용 시

- 입고 시 단가 재계산
- 가격차이 계정 사용 없음
- 재고 금액이 직접 변경됨

---

## 7. 출고 (261 예시)

차변
- 비용 계정 (GBB)

대변
- 재고자산 (BSX)

Dr. Cost of Goods
Cr. Inventory

---

## 8. 통합 핵심 구조

MM 이벤트
→ Movement Type
→ Transaction Key (OBYC)
→ G/L 계정
→ FI 전표 생성

---

## 9. 실무 포인트

- 수량 문제 → Material Document 확인
- 금액 문제 → Accounting Document 확인
- GR/IR 잔액은 회계 리스크
- Price Control(S/V)이 분개 방식에 직접 영향

---

## 10. 면접 대비 답변 구조

질문:
"MM과 FI는 어떻게 연결되나요?"

답변:
- Movement Type 기반 자동 계정결정
- OBYC Transaction Key 매핑
- BSX/WRX/PRD 중심 구조 설명
- GR/IR 상계 흐름까지 설명
