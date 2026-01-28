# SAP MM Output Determination (출력 결정) 정리

## 1. Output Determination이란?
- 구매 문서 생성/변경 시 출력(인쇄, 이메일, EDI 등)을 제어하는 기능
- 발주서, 계약서, 변경 통지 등 자동 발송에 사용

---

## 2. Output의 목적
- 공급업체에 문서 전달
- 구매 변경 사항 자동 통보
- 업무 자동화 및 오류 감소

---

## 3. Output 유형
- Print : 프린터 출력
- External Send : 이메일, 팩스
- EDI : 시스템 간 전자 문서 교환

---

## 4. Output Determination 구성 요소
- Output Type : 출력 문서 종류
- Condition Record : 출력 조건
- Transmission Medium : 전송 방식
- Timing : 즉시/저장 시/백그라운드

---

## 5. 적용 대상 문서
- Purchase Order (PO)
- Contract
- Scheduling Agreement

---

## 6. 실무 포인트
- 출력 안 되는 이슈의 대부분은 Condition Record 누락
- 변경 출력 여부 설정 확인 필수
- 테스트 시 출력 시점(Timing) 주의
- 컨설턴트는 “왜 출력이 안 됐는지” 설명 가능해야 함