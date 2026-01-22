# SAP MM Release Procedure vs Release Strategy 비교

## 1. Release Procedure란?
- SAP의 승인 프로세스 설계 방식
- 어떤 구조로 승인 로직을 구성할지 결정

종류:
- Classic Release Procedure
- Flexible Workflow (S/4HANA)

---

## 2. Release Strategy란?
- 실제 승인 규칙(조건 + 승인자)의 집합
- 금액, 조직 조건에 따라 승인 흐름 정의

구성 요소:
- Release Group
- Release Strategy
- Release Code
- Release Indicator

---

## 3. Classic Release Procedure 특징
- ECC 및 기존 시스템에서 사용
- 조건 기반 승인 로직
- PR / PO 모두 적용 가능

장점:
- 구조 단순
- 안정적

단점:
- 유연성 제한
- 조건 확장 어려움

---

## 4. Flexible Workflow (S/4HANA)
- S/4HANA 표준 승인 방식
- BRF+ 기반
- UI(Fiori)와 연계

장점:
- 조건 확장 용이
- 승인 단계 유연
- 유지보수 편리

---

## 5. Strategy vs Procedure 관계
- Procedure : 승인 구조(틀)
- Strategy  : 실제 승인 규칙(내용)

---

## 6. 실무 포인트
- ECC → Strategy 중심
- S/4HANA → Workflow 중심 전환 중
- 신규 프로젝트는 Workflow 고려 필수
- 컨설턴트는 “어떤 승인 방식인지” 구분 가능해야 함
