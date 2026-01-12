# SAP MM 구매 정보 레코드 (Purchasing Info Record) 심화

## 1. Info Record란?
- 특정 자재(Material)와 특정 공급업체(Vendor) 간의 구매 조건을 저장
- 가격, 납기, 최소 주문 수량 등 반복 조건 관리
- PR/PO 생성 시 자동으로 조건 제안

---

## 2. Info Record 유형
- Standard : 일반 구매
- Subcontracting : 외주 가공
- Consignment : 위탁 재고
- Pipeline : 파이프라인 자재

---

## 3. Info Record 구성
- General Data : 공급업체, 자재 공통 정보
- Purchasing Organization Data : 구매조직별 가격/조건
- Plant Data : 플랜트별 납기/구매 설정

대표 테이블:
- EINA : 일반 데이터
- EINE : 구매조직/플랜트 데이터

---

## 4. 가격 결정과의 관계
- Condition Record 형태로 가격 유지
- PB00(기본가격) 등 Condition Type 사용
- 유효기간 관리 중요

---

## 5. PR/PO에서의 동작
- 자재 + 공급업체 선택 시 Info Record 자동 참조
- 가격/납기 자동 제안
- Source List와 함께 공급업체 결정에 영향

---

## 6. 실무 포인트
- 가격 안 잡히면 Info Record 존재 여부부터 확인
- 구매조직/플랜트 불일치로 미적용 사례 다수
- 유효기간 만료 주의
- 컨설턴트는 “왜 이 가격이 나왔는지” 설명 가능해야 함
