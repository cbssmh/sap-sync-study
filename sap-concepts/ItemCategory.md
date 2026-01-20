# SAP MM Item Category(품목 범주) 정리

## 1. Item Category란?
- 구매 문서의 각 품목(Item)이 어떻게 처리될지 결정하는 설정
- 재고 관리 여부, 계정 전기 방식에 영향

---

## 2. Item Category의 역할
- 재고 관리 대상 여부 결정
- 계정 지정 방식 제어
- 문서 처리 흐름 차별화

---

## 3. 주요 Item Category

### Standard Item
- 일반 자재 구매
- 재고 관리 O
- 가장 기본적인 품목 범주

---

### Consignment Item
- 위탁 재고 구매
- 사용 시점에만 비용 발생
- 재고는 공급업체 소유

---

### Subcontracting Item
- 외주 가공 품목
- 자재 제공 + 가공비 처리
- 특수 Movement Type 사용

---

### Service Item
- 서비스 구매
- 재고 관리 X
- 비용 계정 직접 전기

---

## 4. Item Category 결정 요소
- Purchasing Document Type
- Material Type
- Account Assignment Category

---

## 5. 실무 포인트
- 서비스 품목을 재고로 처리하는 오류 빈번
- 외주 가공 시 Item Category 설정 필수
- 계정 전기 오류의 주요 원인 중 하나
- 컨설턴트는 “왜 재고가 안 잡히는지” 설명 가능해야 함
