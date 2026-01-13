# SAP MM Source List 심화 정리

## 1. Source List란?
- 자재(Material)에 대해 사용 가능한 공급업체(Source)를 관리하는 목록
- 구매 시 어떤 공급업체를 사용할 수 있는지 제어
- 자동 소싱 및 구매 통제에 핵심 역할

---

## 2. Source List의 목적
- 승인된 공급업체만 사용하도록 제한
- 우선 공급업체 지정
- 구매 오류 및 비표준 구매 방지

---

## 3. Source List 주요 속성
- Vendor : 공급업체
- Validity Period : 유효기간
- Fixed Vendor : 고정 공급업체 여부
- Source of Supply : 사용 가능 여부

---

## 4. Fixed Vendor 개념
- 고정 공급업체로 지정 시
  · PR/PO 생성 시 자동 제안
  · 다른 공급업체 선택 제한 가능

---

## 5. Info Record / Quota와의 관계
- Info Record : 가격/조건 정보
- Source List : 사용 가능 공급업체 범위
- Quota Arrangement : 공급 비율 분배
→ 세 설정이 함께 작동해 공급업체 결정

---

## 6. 실무 적용 포인트
- Source List 필수 설정 시, 미유지하면 PO 생성 불가
- 유효기간 만료로 공급업체 미선택 이슈 빈번
- Fixed Vendor 설정 여부 반드시 확인
- 컨설턴트는 “왜 이 공급업체가 선택됐는지” 설명 가능해야 함
