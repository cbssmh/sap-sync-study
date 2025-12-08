# SAP MM Overview (자재관리 개요)

## 1. MM이란?
- SAP의 자재관리(Materials Management) 모듈.
- 구매(Purchasing)와 재고관리(Inventory Management)를 담당.

## 2. MM의 주요 프로세스
- PR → PO → GR → IV → Payment (P2P 흐름)
- 구매요청 → 구매오더 → 입고 → 송장처리 → 지불

## 3. 주요 마스터데이터
- Material Master (자재마스터)
- Vendor Master (공급업체 정보)
- Info Record (자재 + 공급업체 조합)
- Source List (공급업체 우선순위 정보)

## 4. 주요 조직단위
- Company Code (회사)
- Plant (공장/물류센터)
- Storage Location (저장위치)
- Purchasing Organization (구매조직)
- Purchasing Group (구매 담당자)

## 5. MM에서 자주 쓰는 테이블
- MARA : 자재 기본정보
- MARC : 플랜트별 자재정보
- EKKO : 구매오더 헤더
- EKPO : 구매오더 아이템
- MSEG : 자재문서 아이템
- MKPF : 자재문서 헤더

## 6. MM이 중요한 이유
- 모든 제조·유통 기업의 핵심 프로세스
- 재고/구매/회계와 연결되는 중심 모듈
- 실제 SAP 프로젝트에서 가장 많이 사용되는 영역 중 하나
