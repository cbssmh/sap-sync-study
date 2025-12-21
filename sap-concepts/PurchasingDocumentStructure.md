# SAP MM 구매 문서 구조 정리 (PR / PO)

## 1. 구매 문서 개요
- SAP MM의 구매 문서는 Header + Item 구조
- 하나의 문서에 여러 품목(Item)을 가질 수 있음
- PR, PO 모두 동일한 구조 개념 사용

---

## 2. Header (헤더)
- 문서 전체에 공통으로 적용되는 정보
- 문서 단위 속성

주요 정보:
- 문서번호
- Company Code
- Purchasing Organization
- Purchasing Group
- Vendor (PO의 경우)
- 문서일자, 통화

대표 테이블:
- PR Header : EBAN
- PO Header : EKKO

---

## 3. Item (아이템)
- 실제 구매 대상 품목 정보
- 자재, 수량, 단가 등 품목별로 달라지는 정보

주요 정보:
- Material
- Quantity
- Unit
- Price
- Plant
- Storage Location
- Delivery Date

대표 테이블:
- PR Item : EBAN
- PO Item : EKPO

---

## 4. PR 문서 구조
- 구매 요청 단계
- 가격·업체 정보 없이 생성 가능
- 승인 프로세스와 연계됨

구조:
- Header : 요청자, 조직 정보
- Item : 자재, 수량, 플랜트

---

## 5. PO 문서 구조
- 공급업체에 대한 공식 발주 문서
- 계약적 효력 발생

구조:
- Header : Vendor, 구매조직, 결제조건
- Item : 자재, 수량, 가격, 납기

---

## 6. 실무 포인트
- 오류 분석 시 Header 문제인지 Item 문제인지 먼저 구분
- 가격 오류는 대부분 Item 레벨
- 조직 오류는 Header 레벨에서 발생하는 경우가 많음
- 개발/조회 시 Header–Item Join(EKKO–EKPO)이 기본
