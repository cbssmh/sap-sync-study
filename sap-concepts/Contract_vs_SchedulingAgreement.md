# SAP MM 구매 계약(Contract) vs 스케줄링 협약(Scheduling Agreement)

## 1. 공통 개념
- 장기적인 구매 약정을 관리하는 문서
- 반복 구매 시 PO 생성 단순화
- 가격/조건을 사전에 합의

---

## 2. Contract (구매 계약)
- 총 수량 또는 총 금액 기준 계약
- 필요 시점에 PO를 개별 생성

특징:
- 수량/금액 한도 관리
- 유연한 발주 가능

대표 T-Code:
- ME31K : 계약 생성
- ME32K : 계약 변경

---

## 3. Scheduling Agreement (스케줄링 협약)
- 납품 일정(Schedule Line)을 미리 계획
- PO 없이 납품 스케줄 기반으로 자동 처리

특징:
- 정기/반복 납품에 적합
- 생산 계획과 강하게 연계

대표 T-Code:
- ME31L : 스케줄링 협약 생성
- ME32L : 변경

---

## 4. Contract vs Scheduling Agreement 비교
- Contract:
  · 필요 시 PO 생성
  · 유연성 높음
  · 비정기 구매에 적합

- Scheduling Agreement:
  · 납품 일정 고정
  · 자동화 수준 높음
  · 정기 납품에 적합

---

## 5. 실무 선택 기준
- 수요 변동 큼 → Contract
- 정기 납품/대량 → Scheduling Agreement

---

## 6. 실무 포인트
- 계약 유형 선택 오류 빈번
- 스케줄링 협약은 MRP와 강하게 연계
- 가격/조건 변경 시 영향 범위 확인 필수
- 컨설턴트는 “왜 이 문서를 썼는지” 설명 가능해야 함
