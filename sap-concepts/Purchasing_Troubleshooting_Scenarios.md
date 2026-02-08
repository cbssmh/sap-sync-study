# SAP MM 구매 오류 트러블슈팅 시나리오

## 1. PR 생성이 안 되는 경우
원인:
- MRP 미실행 또는 MRP 유형 ND
- Material Master MRP View 누락
- Source of Supply 미결정

조치:
- MRP 실행(MD02)
- MRP View/Source List 확인

---

## 2. PO 생성 시 가격이 안 잡히는 경우
원인:
- Info Record 없음 또는 유효기간 만료
- Condition Record 누락
- Pricing Procedure 결정 오류

조치:
- Info Record/Condition 유지
- Pricing Procedure 결정 키 확인

---

## 3. PO 승인(Release)이 안 되는 경우
원인:
- 승인 조건 미충족
- 승인자 미할당
- 문서 유형 불일치

조치:
- 금액/조건 비교
- Release Strategy 매핑 확인

---

## 4. 입고(GR)가 안 되는 경우
원인:
- PO 미승인
- Item Category/Account Assignment 오류
- Storage Location 오류

조치:
- 승인 상태 확인
- 품목 범주/조직 단위 점검

---

## 5. 송장(IR)이 블로킹되는 경우
원인:
- 수량/가격 불일치
- 허용 오차 초과
- GR 미처리

조치:
- GR/IR 비교
- MRBR로 블록 사유 확인

---

## 6. GR/IR 잔액이 남는 경우
원인:
- 입고 후 송장 미처리
- 송장 금액 차이
- 반품/취소 미정리

조치:
- MIRO/MR11 확인
- 반품 문서 흐름 점검

---

## 7. 실무 트러블슈팅 순서
1) 마스터 데이터
2) 소싱 데이터
3) 가격/계정
4) 승인 상태
5) 물류/회계 문서

→ 위 순서로 점검하면 대부분 해결 가능
