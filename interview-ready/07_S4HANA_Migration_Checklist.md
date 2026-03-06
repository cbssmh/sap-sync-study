# SAP S/4HANA Migration Checklist – MM (Interview Version)

## 1. Migration 개요

ECC → S/4HANA 전환 시  
기능 변화보다 **데이터 모델 변화 영향 분석**이 핵심이다.

MM 영역에서는 다음 4가지가 가장 중요하다.

- Business Partner 전환
- 데이터 모델 변경 (MATDOC)
- 승인 프로세스 변경
- 커스텀 프로그램 영향 분석

---

## 2. Master Data 영향

### Vendor → Business Partner 전환

ECC:
Vendor Master

S/4HANA:
Business Partner

전환 시 확인

- BP Role 매핑
- Vendor 번호 정합성
- 기존 인터페이스 영향

---

### Material Master 점검

확인 항목

- 불필요 View 정리
- Valuation Class 정상 매핑
- MRP 설정 재검증

---

## 3. 데이터 모델 변경 영향

대표 예

ECC:
MSEG

S/4HANA:
MATDOC

영향

- Z 프로그램 직접 테이블 접근 수정
- 집계 테이블 의존 로직 제거
- 리포트 성능 재검증

---

## 4. 승인 프로세스

ECC:
Classic Release Strategy

S/4HANA:
Flexible Workflow 권장

검토 사항

- 기존 승인 전략 유지 여부
- Workflow 재설계 필요 여부

---

## 5. Output Management

ECC:
Message Control

S/4HANA:
BRF+ 기반 Output Management

확인 항목

- 기존 Condition Record
- 출력 타이밍 설정
- 인터페이스 영향

---

## 6. 인터페이스 영향

확인 대상

- RFC
- IDoc
- BDC 프로그램
- Z 인터페이스

특히

- 직접 테이블 접근 여부
- MATDOC 영향

---

## 7. 테스트 전략

Migration 프로젝트 필수 테스트

- Unit Test
- Integration Test
- Data Validation
- Cutover Rehearsal

---

## 8. 면접용 40초 답변

"ECC에서 S/4HANA로 전환할 때
MM에서는 데이터 모델 변화가 가장 큰 영향입니다.

특히 MATDOC 도입으로 기존 재고 테이블 구조가 바뀌며,
Vendor는 Business Partner로 통합됩니다.

또한 승인 프로세스는 Flexible Workflow로 전환될 수 있기 때문에
마스터 데이터와 커스텀 프로그램 영향 분석이 중요합니다."
