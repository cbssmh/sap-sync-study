# SAP MM 구매 프로세스 전체 시나리오 (End-to-End)

## 1. 구매 프로세스 개요
- 자재/서비스 필요 발생부터 지급까지의 전체 흐름
- MM과 FI가 연계되는 대표적인 비즈니스 프로세스

---

## 2. 전체 흐름 요약
요청 → 발주 → 입고 → 송장 → 지급

---

## 3. 단계별 상세

### 1) Purchase Requisition (PR)
- 구매 요청 생성
- 필요 수량/플랜트 입력
- 승인(Release Strategy) 대상

주요 T-Code:
- ME51N / ME52N

---

### 2) Purchase Order (PO)
- 공급업체에 공식 발주
- 가격/납기 확정
- 출력(Output Determination) 발생 가능

주요 T-Code:
- ME21N / ME22N

---

### 3) Goods Receipt (GR)
- 자재 입고 처리
- 재고 증가
- 회계 전표 자동 생성

주요 T-Code:
- MIGO (101)

---

### 4) Invoice Receipt (IR)
- 공급업체 송장 검증
- PO/GR 기준 3-Way Match
- GR/IR 계정 정리

주요 T-Code:
- MIRO

---

### 5) Payment
- 지급 실행 (FI 영역)
- 지급 완료 후 프로세스 종료

---

## 4. 문서 흐름 연결
- PR → PO → Material Document → Accounting Document → Invoice
- 모든 단계가 문서로 연결되어 추적 가능

---

## 5. 주요 체크 포인트
- 승인 누락 여부
- 가격/수량 불일치
- GR/IR 잔액
- 출력/송장 블로킹 여부

---

## 6. 실무 포인트
- 문제 발생 시 단계별로 끊어서 분석
- “어디까지 진행됐는지”가 핵심 질문
- 컨설턴트는 전체 흐름을 한 번에 설명 가능해야 함