# SAP MM End-to-End Process (Interview Version)

## 1. 전체 흐름 요약

PR → PO → GR → IR → FI Posting → Payment

MM은 “수량 흐름”을,
FI는 “금액 흐름”을 관리한다.

---

## 2. 단계별 핵심 설명

### ① Purchase Requisition (PR)

- 내부 구매 요청 문서
- MRP 또는 수동 생성
- 승인 전략 대상

핵심 질문 대응:
> PR은 회계 전표가 발생하지 않음 (약정 단계)

---

### ② Purchase Order (PO)

- 공급업체에 대한 공식 발주 문서
- 가격결정(Pricing Procedure) 적용
- 승인 완료 후 출력 가능

핵심 포인트:
- 가격은 Condition Technique 기반
- 승인 전략과 직접 연결

---

### ③ Goods Receipt (GR) – Movement Type 101

- 재고 수량 증가
- 회계 전표 자동 생성

분개 구조:
Dr. Inventory (BSX)  
Cr. GR/IR (WRX)

→ 수량 + 금액 동시에 반영

---

### ④ Invoice Receipt (IR)

- 3-Way Match 수행
  (PO / GR / Invoice)

정상 처리 시:
Dr. GR/IR  
Cr. Vendor

→ GR/IR 상계 완료

---

### ⑤ Payment

- FI 영역에서 지급 실행
- MM 프로세스 종료

---

## 3. 통합 관점 핵심

MM 이벤트 발생
→ Movement Type
→ Transaction Key
→ OBYC 매핑
→ FI 전표 생성

즉,
MM은 물류,
FI는 금액을 담당하며
자동 계정결정이 연결 고리다.

---

## 4. 실무에서 가장 중요한 질문

### Q1. 가격 오류는 어디서 발생하는가?
→ Pricing Procedure / Condition Record

### Q2. 승인 안 되는 이유는?
→ Release Strategy / Workflow

### Q3. GR/IR 잔액이 왜 남는가?
→ 입고/송장 시점 차이 또는 금액 차이

### Q4. 재고는 있는데 PR이 왜 생성되는가?
→ MRP 파라미터 (Safety Stock / Lead Time)

---

## 5. 면접용 30초 요약 답변

"SAP MM의 End-to-End 프로세스는  
PR에서 시작해 PO, GR, IR을 거쳐 FI 전표까지 연결됩니다.  
GR 시 재고와 GR/IR이 발생하고,  
IR 시 GR/IR이 Vendor로 상계됩니다.  
계정결정은 OBYC와 Valuation Class 기반이며,  
가격결정은 Condition Technique로 처리됩니다."

---

## 6. 이 문서의 목적

- End-to-End 구조 명확화
- MM–FI 통합 이해 증명
- 면접 즉답 가능 구조 확보
