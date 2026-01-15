# SAP MM Special Procurement Type 정리

## 1. Special Procurement Type이란?
- 자재 조달 방식을 일반 구매와 다르게 처리하는 설정
- 자재가 어떻게 조달·이동되는지를 결정

---

## 2. Special Procurement Type 사용 목적
- 외주 가공, 위탁 재고, 타 플랜트 조달 등
- 표준 구매 프로세스로 처리하기 어려운 경우 대응

---

## 3. 대표적인 Special Procurement Type

### Subcontracting (외주 가공)
- 자재를 외주업체에 보내 가공 후 납품
- 외주업체에 자재 제공 + 가공비 지급

### Consignment (위탁 재고)
- 공급업체 소유 재고를 우리 창고에 보관
- 사용 시점에만 비용 발생

### Stock Transfer (특별 조달)
- 다른 Plant에서 자재 조달
- 내부 조달 프로세스 구현

---

## 4. 설정 위치
- 자재 마스터 MRP View
- Special Procurement Type 필드에서 지정

---

## 5. 관련 Movement Type 예시
- 541 / 543 : 외주 가공 자재 이동
- 411 / 412 : 위탁 재고 사용/취소

---

## 6. 실무 포인트
- Special Procurement Type 설정 누락 시 조달 오류 발생
- MRP 결과에 직접적인 영향
- 회계 처리 방식이 일반 구매와 다를 수 있음
- 컨설턴트는 “왜 이 조달 방식이 쓰였는지” 설명 가능해야 함
