# SAP MM 계정결정 (Account Determination) 정리

## 1. 계정결정이란?
- 재고 이동 시 어떤 회계 계정으로 금액을 전기할지 결정하는 로직
- MM과 FI를 연결하는 핵심 설정

---

## 2. 계정결정이 필요한 이유
- 입고/출고 시 자동으로 회계 전표 생성
- 자재 유형, 이동유형에 따라 다른 계정 사용
- 잘못되면 금액이 엉뚱한 계정으로 전기됨

---

## 3. 계정결정의 주요 기준
- Valuation Class (평가 클래스)
- Movement Type (이동유형)
- Transaction Key (트랜잭션 키)

---

## 4. 주요 Transaction Key 예시
- BSX : 재고 계정
- WRX : GR/IR 계정
- GBB : 출고/차이 계정
- PRD : 가격 차이 계정

---

## 5. 기본 흐름
1) 자재 이동 발생 (예: 101 입고)
2) Movement Type 확인
3) Valuation Class 확인
4) Transaction Key 매핑
5) 해당 G/L 계정으로 전기

---

## 6. 실무 포인트
- 계정 오류 문의의 대부분은 계정결정 문제
- Valuation Class 설정 누락 여부 먼저 확인
- 신규 자재 생성 시 계정결정 테스트 필수
- 컨설턴트는 “왜 이 계정으로 갔는지” 설명 가능해야 함
