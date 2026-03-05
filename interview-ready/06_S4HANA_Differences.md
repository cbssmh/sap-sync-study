# SAP ECC vs S/4HANA – MM 주요 차이 (Interview Version)

## 1. S/4HANA 개요

S/4HANA는 SAP의 차세대 ERP 플랫폼으로  
HANA 인메모리 데이터베이스 기반으로 설계된 시스템이다.

핵심 특징

- 데이터 모델 단순화
- 실시간 처리 성능 개선
- Fiori 기반 UI
- 프로세스 자동화 강화

---

## 2. 데이터 모델 변화

ECC:
- 다수의 테이블 구조
- 집계 테이블 존재

S/4HANA:
- 데이터 모델 단순화
- MATDOC 통합 테이블 도입

예:
MSEG + 일부 집계 테이블 → MATDOC

효과:
- 재고 계산 실시간 처리
- 테이블 구조 단순화

---

## 3. Business Partner 통합

ECC:
- Vendor / Customer 별도 관리

S/4HANA:
- Business Partner(BP)로 통합 관리

트랜잭션:
BP

---

## 4. 승인 프로세스 변화

ECC:
Classic Release Strategy

S/4HANA:
Flexible Workflow

특징

- BRF+ 기반
- Fiori 승인
- 조건 확장 용이

---

## 5. Output Management 변화

ECC:
Message Control

S/4HANA:
BRF+ 기반 Output Management

특징

- 설정 구조 단순화
- UI 기반 관리

---

## 6. MRP 변화

MRP Live 도입

특징

- HANA 기반 고속 계산
- 대량 자재 동시 실행 가능

---

## 7. 실무 영향

컨설턴트 관점 핵심 변화

- Business Partner 전환
- Flexible Workflow 승인
- MATDOC 데이터 모델
- Output Management 변경

---

## 8. 면접용 40초 답변

"S/4HANA에서는 데이터 모델 단순화가 가장 큰 변화입니다.
예를 들어 재고 관련 테이블이 MATDOC으로 통합되었습니다.
또한 Vendor와 Customer가 Business Partner로 통합되었고,
승인 프로세스는 Classic Release Strategy 대신
Flexible Workflow 기반으로 구성됩니다."
