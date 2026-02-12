# SAP S/4HANA MM 주요 차이점 정리

## 1. S/4HANA란?
- SAP의 차세대 ERP 플랫폼
- HANA 인메모리 DB 기반
- 단순화(Simplification)와 실시간 처리 강화

---

## 2. ECC vs S/4HANA 구조 차이
- ECC: 다수의 개별 테이블 구조
- S/4HANA: 데이터 모델 단순화

예:
- MATDOC 테이블 도입 (재고 통합)
- 일부 Aggregate/Index 테이블 제거

---

## 3. MRP 변화
- MRP Live 도입
- HANA 기반 고속 처리
- 대량 자재 동시 실행 성능 개선

---

## 4. 승인 프로세스 변화
- ECC: Classic Release Strategy
- S/4HANA: Flexible Workflow (BRF+ 기반)

→ Fiori 승인 화면 사용

---

## 5. Output Management 변화
- ECC: Message Control
- S/4HANA: BRF+ 기반 Output Management
- 설정 방식 단순화 및 UI 개선

---

## 6. Fiori UI 도입
- GUI 중심 → Fiori 앱 기반
- 사용자 친화적 인터페이스
- 승인/모니터링 기능 강화

---

## 7. 데이터 모델 단순화 예시
- Business Partner(BP) 통합
  · Vendor/Customer 통합 관리

---

## 8. 실무 포인트
- 신규 프로젝트는 S/4HANA 기준 이해 필수
- Classic 설정과 Workflow 차이 구분 필요
- 단순 기능보다 데이터 모델 변화 이해 중요
- 컨설턴트는 ECC와의 차이 설명 가능해야 함