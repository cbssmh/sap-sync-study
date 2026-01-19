# SAP MM 구매 문서 유형 (Purchasing Document Type) 정리

## 1. 구매 문서 유형이란?
- PR, PO 등 구매 문서의 성격을 정의하는 설정
- 문서 번호 체계, 승인 여부, 필드 제어 등에 영향

---

## 2. 구매 문서 유형의 목적
- 구매 프로세스 표준화
- 문서 성격별 통제(승인, 변경 제한)
- 회사 정책 반영

---

## 3. 주요 구매 문서 유형

### Purchase Requisition (PR)
- NB : 표준 구매요청
- FO : 프레임워크 요청(예시)

---

### Purchase Order (PO)
- NB : 표준 구매오더
- UB : 재고 이전용 PO (Stock Transfer)
- FO : 프레임 계약 기반 PO
- Z*** : 회사별 커스텀 유형

---

## 4. 문서 유형별 제어 항목
- Number Range (문서 번호 범위)
- Release Strategy (승인 필요 여부)
- Field Selection (필수/선택/숨김 필드)
- Allowed Item Category

---

## 5. 문서 유형 선택 기준
- 일반 구매 → NB
- 내부 재고 이전 → UB
- 장기 계약 구매 → 계약/스케줄링 문서

---

## 6. 실무 포인트
- 잘못된 문서 유형 선택 = 승인/회계 오류
- UB와 NB 혼동 사례 빈번
- 신규 유형 생성 시 승인/번호체계 검토 필수
- 컨설턴트는 “왜 이 문서 유형을 쓰는지” 설명 가능해야 함
