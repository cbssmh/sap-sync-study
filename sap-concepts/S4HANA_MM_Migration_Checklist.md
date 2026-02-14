# SAP S/4HANA 전환 시 MM 체크리스트

## 1. 전환 개요
- ECC → S/4HANA 마이그레이션 시
- 기능, 데이터 모델, 인터페이스 영향 분석 필수

---

## 2. 마스터 데이터 점검

### Material Master
- 불필요한 뷰 정리
- Valuation Class 정상 매핑 확인
- MRP 설정 재검증

### Vendor → Business Partner 전환
- BP 역할(Role) 매핑 확인
- 기존 Vendor 번호 정합성 점검

---

## 3. 조직 구조 점검
- Company Code / Plant 구조 유지 여부
- Purchasing Organization 연결 구조 재검토

---

## 4. 가격 및 조건 점검
- Pricing Procedure 영향 분석
- Condition Record 유효성 확인
- Output Management 전환 대응

---

## 5. 승인 프로세스 점검
- Classic Release 유지 여부 결정
- Flexible Workflow 도입 검토
- 승인 조건 재설계 필요 여부 분석

---

## 6. 인터페이스 점검
- IDoc / RFC 영향 분석
- Z 프로그램 테이블 직접 접근 여부 확인
- MATDOC 전환 대응

---

## 7. 리포트 및 커스텀 프로그램
- 제거된 테이블 사용 여부 확인
- 집계 테이블 의존 프로그램 수정 필요
- 성능 테스트 필수

---

## 8. 테스트 전략
- 단위 테스트
- 통합 테스트
- 데이터 마이그레이션 검증
- Cutover 리허설

---

## 9. 실무 포인트
- 기술 전환보다 데이터 영향 분석이 핵심
- BP 전환이 가장 큰 변화
- Z 프로그램 영향 분석이 리스크 포인트
- 컨설턴트는 “어디가 가장 위험한지” 설명 가능해야 함
