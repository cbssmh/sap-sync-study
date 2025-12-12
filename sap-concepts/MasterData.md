# SAP MM Master Data 정리

## 1) Master Data란?
- SAP에서 반복적으로 사용되는 기준 정보
- 거래 데이터(PR, PO, GR 등)의 기반이 됨
- 정확하지 않으면 프로세스 전체에 오류 발생

---

## 2) Material Master (자재 마스터)
- 자재에 대한 모든 기본 정보
- 여러 조직단위에서 공통으로 사용

주요 뷰:
- Basic Data: 자재명, 단위
- Purchasing: 구매 관련 정보
- MRP: 자재 소요 계획
- Accounting: 자산/재고 평가

대표 테이블:
- MARA (자재 기본)
- MARC (플랜트별 자재)

---

## 3) Vendor Master (공급업체 마스터)
- 공급업체 기본 정보 관리
- MM과 FI에서 함께 사용

대표 테이블:
- LFA1 (공급업체 일반 정보)
- LFB1 (회사코드별 정보)

---

## 4) Purchasing Info Record
- 특정 자재 + 특정 공급업체 조합 정보
- 가격, 납기, 최소 주문 수량 관리

대표 테이블:
- EINA
- EINE

---

## 5) Source List
- 자재별 사용 가능한 공급업체 목록
- 우선 공급업체 지정 가능

---

## 6) Master Data가 중요한 이유
- PR/PO 생성의 기준 데이터
- 가격 오류, 입고 오류의 원인이 되기 쉬운 영역
- MM 컨설턴트가 가장 많이 다루는 설정 영역
