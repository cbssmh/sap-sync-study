# SAP MM Quota Arrangement 정리

## 1. Quota Arrangement란?
- 동일 자재를 여러 공급업체로부터 구매할 때
  구매 비율을 정해 자동으로 분배하는 기능
- 공급 리스크 분산 목적

---

## 2. Quota Arrangement 사용 목적
- 특정 공급업체 의존도 감소
- 가격/납기 리스크 분산
- 자동 소싱 로직 구현

---

## 3. Quota 구성 요소
- Vendor : 공급업체
- Quota : 구매 비율 값
- Quota Base Quantity : 기준 수량
- Allocated Quantity : 이미 배정된 수량

---

## 4. 동작 원리
- Quota Rating = Allocated Quantity / Quota
- 가장 낮은 Rating을 가진 공급업체가 선택됨
- 구매 진행 시 Allocated Quantity 자동 증가

---

## 5. Source List / Info Record와의 관계
- Source List : 사용 가능한 공급업체 범위 제한
- Info Record : 가격/조건 제공
- Quota Arrangement : 공급 비율 결정
→ 세 설정이 함께 작동해야 정상 동작

---

## 6. 실무 포인트
- Quota 설정 후 테스트 구매 필수
- Allocated Quantity 초기화 여부 주의
- Source List 미설정 시 Quota 미적용 가능
- 컨설턴트는 “왜 이 공급업체가 선택됐는지” 설명 가능해야 함
