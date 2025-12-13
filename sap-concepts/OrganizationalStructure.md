# SAP MM 조직구조(Organizational Structure) 정리

## 1) 조직구조란?
- SAP에서 업무와 데이터를 구분·관리하기 위한 기준 단위
- MM, FI, SD 등 모든 모듈의 기본 뼈대
- 조직구조가 잘못되면 프로세스 전체가 꼬임

---

## 2) Client
- SAP 시스템의 최상위 단위
- 하나의 시스템 안에서 논리적으로 완전히 분리된 환경
- 예: 개발 / 테스트 / 운영 Client

---

## 3) Company Code (회사코드)
- 하나의 법인 단위
- 재무회계(FI)의 기준 단위
- 재무제표는 Company Code 기준으로 생성됨

---

## 4) Plant
- 생산 공장 또는 물류 거점
- MM에서 가장 중요한 조직 단위
- 재고는 Plant 단위로 관리됨

---

## 5) Storage Location
- Plant 내부의 세부 창고
- 자재가 실제로 보관되는 위치
- 재고 이동, 입고/출고 시 사용

---

## 6) Purchasing Organization
- 구매를 담당하는 조직 단위
- Company Code 또는 Plant에 연결됨
- 구매 정책과 계약의 기준

---

## 7) Purchasing Group
- 실제 구매 담당자 또는 팀
- 사람 중심의 조직 단위
- 보고 및 책임 구분용

---

## 8) 조직구조 관계 요약
- Client
  └ Company Code
      └ Plant
          └ Storage Location

- Purchasing Organization
- Purchasing Group

---

## 9) MM에서 조직구조가 중요한 이유
- PR / PO 생성 시 필수 입력값
- 가격, 공급업체, 재고 관리 기준이 됨
- 오류 발생 시 조직구조 설정 문제인 경우가 매우 많음
