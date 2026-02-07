# SAP MM 구매 데이터 정합성 체크 포인트

## 1. 데이터 정합성이란?
- 구매 프로세스 전반에서 데이터가 서로 모순 없이 일관되게 유지되는 상태
- 오류 대부분은 데이터 불일치에서 발생

---

## 2. 마스터 데이터 체크

### Material Master
- Purchasing View / MRP View 누락 여부
- Plant/Storage Location 일치 여부
- Price Control(표준가/이동평균가) 확인

### Vendor Master
- 구매조직 확장 여부
- 지불조건/통화 설정 확인
- Block 상태 여부

---

## 3. 소싱 데이터 체크
- Source List 유효기간/Fixed Vendor
- Info Record 존재 여부 및 유효기간
- Quota Arrangement 설정 일관성

---

## 4. 가격/계정 체크
- Pricing Procedure 결정 정상 여부
- Condition Record 누락 여부
- Valuation Class / Account Determination 매핑

---

## 5. 문서 레벨 체크
- PR → PO 참조 관계 정상
- 승인 상태(Release) 완료 여부
- 변경 로그(Change History) 확인

---

## 6. 물류/회계 연계 체크
- GR 처리 여부
- GR/IR 잔액 존재 여부
- 송장 블로킹 상태

---

## 7. 실무 포인트
- 오류 발생 시 “마스터 → 소싱 → 가격 → 문서 → 회계” 순으로 점검
- 유효기간/조직 불일치가 가장 흔한 원인
- 컨설턴트는 체크리스트로 원인 축소 가능해야 함