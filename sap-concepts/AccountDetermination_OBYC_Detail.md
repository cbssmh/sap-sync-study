# SAP MM 계정결정 OBYC 설정 상세 정리

## 1. OBYC란?
- Automatic Account Determination 설정 트랜잭션
- 자재 이동 시 어떤 G/L 계정으로 전기할지 결정

트랜잭션:
- OBYC

---

## 2. 기본 개념 구조

자재 이동 발생
→ Movement Type 확인
→ Transaction Key 결정
→ Valuation Class 확인
→ G/L 계정 매핑
→ 회계 전표 생성

---

## 3. 주요 Transaction Key 상세

### BSX – 재고 계정
- 재고 자산 계정
- 입고 시 차변, 출고 시 대변

---

### WRX – GR/IR 계정
- 입고 시 임시 계정
- 송장 처리 시 상계

---

### GBB – 출고/차이 계정
- 소비, 비용 처리
- Movement Type에 따라 일반/스크랩 구분

세부 분류 예:
- VBR : 소비
- AUF : 오더 관련
- INV : 재고 차이

---

### PRD – 가격 차이 계정
- Standard Price 사용 시 발생
- 구매 가격 ≠ 표준가

---

## 4. Valuation Class 연결

자재 마스터(Accounting View)
→ Valuation Class 지정

SPRO
→ MM
→ Valuation and Account Assignment
→ Account Determination
→ Assign Valuation Classes to Account Categories

---

## 5. OBYC 실제 설정 단계

SPRO
→ MM
→ Valuation and Account Assignment
→ Account Determination
→ Configure Automatic Postings

1) Transaction Key 선택
2) Chart of Accounts 지정
3) Valuation Class별 G/L 계정 입력

---

## 6. 예시 시나리오

조건:
- 자재 Valuation Class = 3000
- Movement Type = 101

흐름:
101 → BSX
Valuation Class 3000
→ 재고 계정 140000 전기

---

## 7. 실무에서 자주 발생하는 오류

- Valuation Class 미설정
- G/L 계정 미유지
- 잘못된 Chart of Accounts
- Standard vs Moving Average 오해

---

## 8. 면접 대비 핵심 답변 구조

질문:
"계정결정은 어떻게 이루어지나요?"

답변:
1) OBYC에서 Transaction Key 기준 설정
2) Valuation Class와 매핑
3) Movement Type에 따라 Key 호출
4) G/L 계정 자동 전기
