# SAP MM Message Control vs Output Determination 비교

## 1. Message Control이란?
- SAP에서 출력 및 메시지 전송을 제어하는 기존 프레임워크
- 출력 조건, 전송 방식, 시점을 관리
- 주로 ECC 환경에서 사용

---

## 2. Output Determination이란?
- 문서 생성/변경 시 출력 로직을 관리하는 개념
- Message Control을 기반으로 동작
- PO, 계약, 스케줄링 협약 등 구매 문서에 적용

---

## 3. 두 개념의 관계
- Message Control : 기술적 프레임워크
- Output Determination : 업무 관점의 출력 설정
→ Output Determination은 Message Control을 사용해 구현됨

---

## 4. ECC vs S/4HANA 차이
- ECC:
  · Message Control 중심
  · Condition Record 기반

- S/4HANA:
  · Output Management(BRF+) 도입
  · Flexible Output 설정 가능

---

## 5. 주요 비교 요약
- Message Control:
  · 기술 중심
  · 전통적 구조

- Output Determination:
  · 업무 중심
  · 문서별 출력 제어에 초점

---

## 6. 실무 포인트
- ECC 시스템에서는 Message Control 이해 필수
- S/4HANA 프로젝트는 Output Management 여부 확인
- 출력 오류 시 “프레임워크 vs 설정” 구분 필요
- 컨설턴트는 시스템 버전에 따라 접근 방식 설명 가능해야 함