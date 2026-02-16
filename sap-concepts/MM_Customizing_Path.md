# SAP MM 주요 Customizing 경로 정리 (SPRO 기준)

## 1. 조직 구조 설정

SPRO
→ Enterprise Structure
→ Definition
→ Materials Management
→ Define, Copy, Delete, Check Plant
→ Define Purchasing Organization
→ Define Purchasing Group

---

## 2. 구매 문서 유형 설정

SPRO
→ Materials Management
→ Purchasing
→ Purchase Order
→ Define Document Types

---

## 3. Release Strategy 설정 (Classic)

SPRO
→ Materials Management
→ Purchasing
→ Purchase Order
→ Release Procedure for Purchase Orders

구성 단계:
1) Release Group 정의
2) Release Code 정의
3) Release Indicator 정의
4) Strategy 설정
5) Classification 연결

---

## 4. Pricing Procedure 설정

SPRO
→ Materials Management
→ Purchasing
→ Conditions
→ Define Price Determination Process
→ Define Calculation Schema

관련:
- Condition Type 정의
- Access Sequence 정의
- Schema Determination

---

## 5. Account Determination 설정

SPRO
→ Materials Management
→ Valuation and Account Assignment
→ Account Determination
→ Configure Automatic Postings (OBYC)

핵심:
- Transaction Key (BSX, WRX, GBB 등)
- Valuation Class 매핑

---

## 6. Output Determination (ECC)

SPRO
→ Materials Management
→ Purchasing
→ Messages
→ Output Control

---

## 7. MRP 설정

SPRO
→ Materials Management
→ Consumption-Based Planning
→ MRP Types
→ Define MRP Types

---

## 8. 실무 포인트
- 설정 오류의 대부분은 SPRO 경로 이해 부족에서 발생
- 면접에서 “어디서 설정하나요?” 질문 자주 나옴
- Customizing 경로를 설명할 수 있으면 실무 이해도 인정받음
