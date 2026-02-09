# SAP MM 실무 Q&A 20선

## 1. PR이 생성되지 않아요
- MRP 유형/뷰 설정 확인
- Source of Supply 존재 여부 점검

## 2. PO 가격이 0으로 나와요
- Info Record / Condition Record 유효기간 확인
- Pricing Procedure 결정 키 점검

## 3. 승인 버튼이 안 보여요
- 승인자 권한/Release Code 매핑 확인

## 4. 승인했는데 PO 생성이 안 돼요
- Release Indicator 상태 확인

## 5. GR이 안 됩니다
- PO 승인 완료 여부
- Item Category/Storage Location 확인

## 6. GR 취소는 어떻게 하나요?
- 102 Movement Type 사용

## 7. 송장이 블로킹됐어요
- 가격/수량 차이 확인
- MRBR에서 블록 사유 조회

## 8. GR/IR 잔액이 남아요
- 입고·송장 처리 시점 불일치
- MR11로 차이 정리

## 9. 다른 공급업체가 자동 선택돼요
- Source List / Quota Arrangement 확인

## 10. 가격이 계약과 달라요
- 계약 유효기간 및 우선순위 확인

## 11. 서비스 구매인데 재고가 생겨요
- Item Category / Account Assignment 오류

## 12. 반품 처리 방법은?
- Return PO + Movement Type 122

## 13. 출력이 안 돼요
- Output Condition Record 확인

## 14. 출력이 중복돼요
- Timing 설정 확인

## 15. 재고는 있는데 MRP가 PR을 만들어요
- Safety Stock / Planning Time Fence 점검

## 16. 특정 Plant만 문제예요
- 조직단위/마스터 확장 여부 확인

## 17. 가격 차이가 회계에 잡혀요
- Price Control(S/V) 확인

## 18. 승인 후 가격 변경돼요
- Changeability Indicator 확인

## 19. 특정 사용자만 오류가 나요
- 권한/Role 차이 확인

## 20. 어디부터 봐야 할지 모르겠어요
- 마스터 → 소싱 → 가격 → 승인 → 물류/회계 순으로 점검
