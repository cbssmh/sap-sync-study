# SAP MM 주요 Transaction Code 정리

## 1. Transaction Code(T-Code)란?
- SAP 프로그램을 실행하기 위한 단축 코드
- 업무 처리의 시작점
- MM 실무에서는 T-Code 숙지가 필수

---

## 2. 구매 관련 T-Code

### ME51N – Purchase Requisition 생성
- 구매요청(PR) 생성
- 자재, 수량, 플랜트 입력
- P2P 프로세스의 시작 단계

### ME52N – Purchase Requisition 변경
- 기존 PR 수정

### ME53N – Purchase Requisition 조회
- PR 조회 전용

---

## 3. 구매오더(PO) 관련 T-Code

### ME21N – Purchase Order 생성
- 구매오더(PO) 생성
- 공급업체, 가격, 납기 입력
- 계약적 효력 발생

### ME22N – Purchase Order 변경
- PO 내용 수정

### ME23N – Purchase Order 조회
- PO 조회 전용

---

## 4. 입고 / 자재이동 관련 T-Code

### MIGO – Goods Movement
- 입고(GR), 출고(GI), 이동 처리
- Movement Type(101, 261 등) 선택
- MM 실무에서 가장 많이 사용

---

## 5. 송장 처리 T-Code

### MIRO – Invoice Verification
- 공급업체 송장 처리
- PO / GR 기준으로 금액 확인
- 회계(FI) 전표 생성

---

## 6. 마스터데이터 관련 T-Code

### MM01 – Material Master 생성
### MM02 – Material Master 변경
### MM03 – Material Master 조회

### XK01 – Vendor 생성
### XK02 – Vendor 변경
### XK03 – Vendor 조회

---

## 7. 실무 포인트
- PR → PO → GR → IV 흐름을 T-Code로 연결해서 이해해야 함
- 사용자 문의 대응 시 “어떤 T-Code에서 발생했는지”가 핵심
- 컨설턴트는 최소한 조회/생성 T-Code는 바로 떠올릴 수 있어야 함
