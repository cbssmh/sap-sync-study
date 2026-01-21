# SAP MM Account Assignment Category 정리

## 1. Account Assignment Category란?
- 구매 품목의 비용을 어디에 귀속시킬지 결정하는 설정
- 재고로 관리할지, 비용으로 바로 처리할지 판단

---

## 2. Account Assignment Category의 역할
- 비용 전기 대상 결정
- 재고 관리 여부와 직접 연관
- 회계(FI) 계정 전기의 기준

---

## 3. 주요 Account Assignment Category

### K – Cost Center
- 비용 센터로 전기
- 사무용품, 소모품 등에 사용
- 재고 관리 X

---

### F – Order
- 내부 오더로 전기
- 프로젝트/특정 작업 비용 관리
- 재고 관리 X

---

### A – Asset
- 고정자산으로 전기
- 설비, 장비 구매 시 사용
- 자산 계정으로 처리

---

### P – Project (WBS)
- 프로젝트 단위 비용 관리
- 프로젝트 시스템(PS)와 연계

---

## 4. Item Category와의 관계
- Service Item → Account Assignment 필수
- Standard Item → 재고 구매 시 보통 미사용
- 조합에 따라 허용/비허용 여부 결정됨

---

## 5. 실무 포인트
- Account Assignment 누락 시 PO 저장 불가
- 잘못된 Category 선택 = 회계 오류
- 재고 vs 비용 구분이 핵심 판단 기준
- 컨설턴트는 “왜 비용으로 처리됐는지” 설명 가능해야 함