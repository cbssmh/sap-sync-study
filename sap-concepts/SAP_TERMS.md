# SAP 필수 기초 용어 정리 (입문자용)

## 1. Client(클라이언트)
- SAP 시스템 내의 논리적 구분 단위
- 개발(Client 100), 테스트(Client 200), 운영(Client 300) 같은 구조로 나뉨

## 2. Company Code(회사코드)
- 하나의 독립된 법인을 의미
- 재무(FI) 모듈에서 회계 장부를 관리하는 기준
- 예: 회사 A = 1000, 회사 B = 2000

## 3. Plant(플랜트)
- 제조/생산/물류 거점
- SAP MM·PP·SD에서 매우 중요한 조직 단위
- 예: 서울 공장, 부산 물류센터

## 4. Storage Location(SLoc, 저장위치)
- 플랜트 내의 세부 창고 구역
- 자재가 실제로 보관되는 위치

## 5. Material(자재)
- 원자재/부품/완제품 등 SAP에서 관리하는 품목
- Material Master(자재마스터)로 관리됨

## 6. Vendor(공급업체)
- 물품을 공급하는 외부 업체
- Vendor Master로 정보 관리

## 7. Purchasing Organization(구매조직)
- 회사 내의 구매를 담당하는 조직 단위
- 구매오더(PO) 생성 시 필수

## 8. Purchasing Group(구매그룹)
- 실제 구매 담당자(사람 단위)
- 업무 담당자 식별용

## 9. PR (Purchase Requisition, 구매요청)
- “이거 필요해요!” 라는 내부 요청
- 구매오더 생성 전단계

## 10. PO (Purchase Order, 구매오더)
- 공급업체에 정식으로 발주하는 문서
- 가격/수량/납기 포함

## 11. GR (Goods Receipt, 입고)
- 물건이 실제로 창고에 도착했을 때 처리하는 단계

## 12. IV (Invoice Verification, 송장처리)
- 공급업체가 보낸 송장을 확인하고 회계에 넘기는 과정

## 13. Master Data(마스터데이터)
- 자주 사용하는 기초 정보(자재코드, 업체코드, 고객정보 등)
- SAP에서 가장 중요한 데이터 중 하나

## 14. Transaction Code(T-Code)
- SAP 프로그램 호출을 위한 코드
- 예: ME21N(PO 생성), ME51N(PR 생성)

## 15. Organizational Structure(조직 구조)
- Client → Company Code → Plant → Storage Location 구조
- SAP 시스템의 핵심 개념

## 16. Table(테이블)
- SAP의 모든 데이터가 저장되는 DB 구조
- 예: EKKO(PO 헤더), EKPO(PO 아이템)

## 17. Posting(전표 처리)
- 회계나 구매 단계에서 “데이터 확정” 처리하는 것

## 18. Movement Type(이동유형)
- 자재 이동을 분류하는 코드
- 예: 101(입고), 102(입고 취소)

## 19. BOM(Bill of Materials, 자재 명세서)
- 완제품을 만들기 위해 필요한 부품 리스트

## 20. Routing(라우팅)
- 제조 과정의 작업 순서(생산 쪽 개념)
