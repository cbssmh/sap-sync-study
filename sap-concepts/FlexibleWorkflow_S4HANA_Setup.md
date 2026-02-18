# SAP S/4HANA Flexible Workflow 승인 설정 상세 정리

## 1. Flexible Workflow란?
- S/4HANA에서 제공하는 표준 승인 프레임워크
- Classic Release Strategy의 대안
- Fiori 기반 승인 처리

---

## 2. Classic vs Flexible 차이

Classic:
- Classification 기반
- SPRO 중심 설정
- 구조 고정적

Flexible:
- BRF+ 기반 조건 설정
- 단계 유연 설정
- Fiori 승인 앱 사용

---

## 3. 기본 설정 흐름

1) Workflow 활성화
2) Scenario 정의
3) 조건 정의
4) 승인 단계 정의
5) 담당자(Role) 매핑

---

## 4. 설정 경로

SPRO
→ Cross-Application Components
→ Flexible Workflow

또는 Fiori 앱:
- Manage Workflows for Purchase Orders

---

## 5. Scenario 예시 (PO 승인)

조건:
- 금액 10,000 초과
- 구매조직 1000

단계:
1) 1차 승인 – 팀장
2) 2차 승인 – 부서장

---

## 6. 조건 설정 방식

- Document Type
- Total Net Amount
- Company Code
- Purchasing Group
- Plant

→ 조건 조합으로 승인 흐름 결정

---

## 7. 승인자 결정 방식

- 고정 사용자
- Role 기반
- Manager 관계 기반

---

## 8. 실무 장점

- 조건 확장 쉬움
- 승인 단계 동적 구성 가능
- UI 친화적
- 유지보수 용이

---

## 9. 실무 주의사항

- Classic Strategy와 중복 설정 금지
- 테스트 시 Workflow 로그 확인
- 승인 지연 시 Agent Determination 확인

---

## 10. 면접 대비 핵심 포인트

질문:
"S/4HANA 승인 설정 방식은?"

답변:
- Flexible Workflow 사용
- BRF+ 기반 조건 정의
- Fiori에서 단계 관리
- Classic과 구조적 차이 강조
