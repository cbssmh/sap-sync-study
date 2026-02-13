# SAP S/4HANA MM Simplification Items 정리

## 1. Simplification Item이란?
- ECC 대비 S/4HANA에서 변경/삭제/통합된 기능 목록
- 시스템 전환 시 반드시 검토해야 할 항목

---

## 2. 데이터 모델 단순화

### MATDOC 도입
- 기존 MSEG + 일부 집계 테이블 통합
- 단일 테이블 기반 재고 관리
- 실시간 재고 계산

---

### Aggregate / Index Table 제거
- 중복 저장 구조 제거
- HANA 성능 기반 실시간 계산

---

## 3. Business Partner 통합
- Vendor/Customer 개념 통합
- BP(Transaction: BP)로 관리
- 기존 XK01 → BP 사용

---

## 4. Output Management 변경
- Message Control → BRF+ 기반 Output Management
- Fiori 중심 설정

---

## 5. MRP 변경
- MRP Live 도입
- HANA 최적화
- 일부 Classic 기능 제한

---

## 6. 승인 프로세스 변화
- Classic Release Strategy 유지 가능
- Flexible Workflow 권장

---

## 7. 전환 시 체크 포인트
- 커스텀 Z 프로그램 영향 분석
- 테이블 구조 변경 대응
- BP 전환 전략 수립
- 출력 및 승인 재설계

---

## 8. 실무 포인트
- Simplification Item List 문서 확인 필수
- ECC 경험만으로 접근 시 오류 가능
- S/4HANA 프로젝트는 “기능 + 데이터 모델” 이해 중요
- 컨설턴트는 전환 영향 범위 설명 가능해야 함