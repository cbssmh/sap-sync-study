# SAP MM MRP(Material Requirements Planning) 기본 정리

## 1. MRP란?
- 자재 소요를 계산해 언제, 얼마를 조달할지 계획하는 기능
- 재고 부족/과잉을 방지하는 핵심 로직

---

## 2. MRP의 목적
- 필요한 자재를 필요한 시점에 확보
- 재고 최소화 + 생산/구매 안정성 확보
- 자동 구매/생산 제안 생성

---

## 3. MRP 동작에 필요한 데이터
- Material Master (MRP View)
- 재고 수량
- 소요량(생산 계획, 예약 등)
- 리드타임(납기)

---

## 4. MRP 실행 결과
- Purchase Requisition (구매 제안)
- Planned Order (생산 제안)
- Stock Transfer 제안

---

## 5. 주요 MRP 유형
- PD : 표준 MRP
- VB : 재주문점 기반
- ND : MRP 미실행

---

## 6. 주요 트랜잭션
- MD01 : 전체 MRP 실행
- MD02 : 단일 자재 MRP 실행
- MD04 : 재고/소요량 리스트

---

## 7. 실무 포인트
- MRP 오류의 대부분은 마스터 데이터 문제
- 리드타임/안전재고 설정 중요
- 결과 PR은 자동 생성이지만 검토 필수
- 컨설턴트는 “왜 이 시점에 PR이 생겼는지” 설명 가능해야 함