# SAP MM 승인 프로세스 (Release Strategy) 정리

## 1. Release Strategy란?
- PR 또는 PO를 생성한 후 승인(결재)을 받기 위한 프로세스
- 금액, 조직, 자재 조건 등에 따라 승인자 결정
- 내부 통제 및 결재 절차를 위해 사용

---

## 2. Release Strategy 적용 대상
- Purchase Requisition (PR)
- Purchase Order (PO)

---

## 3. Release Strategy 구성 요소

### Release Code
- 실제 승인자(결재자)
- 한 명 또는 여러 명 가능

### Release Group
- 승인 전략을 묶는 단위
- 문서 유형별로 구분

### Release Indicator
- 승인 상태 표시
- 승인 전 / 승인 후 상태 관리

### Release Condition
- 승인 여부를 결정하는 조건
- 금액, 구매조직, 플랜트 등 기준

---

## 4. 승인 흐름 예시
1) PR 생성 (미승인 상태)
2) 조건 충족 시 승인 대상 지정
3) 승인자 승인 처리
4) 승인 완료 후 PO 생성 가능

---

## 5. 실무 포인트
- 승인 안 되면 다음 단계 진행 불가
- 금액 기준 승인 조건이 가장 흔함
- 사용자 문의 중 “결재가 안 올라간다” 이슈 다수
- 컨설턴트는 조건/승인자/상태를 구분해서 봐야 함
