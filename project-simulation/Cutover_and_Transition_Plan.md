# [프로젝트 시뮬레이션] Cutover & 전환 계획 문서

## 1. Cutover 개요

목적:
- To-Be 프로세스 전환 시 운영 리스크 최소화
- 데이터 정합성 확보
- 안정적 Go-Live 지원

전환 대상:
- 승인 프로세스 (Flexible Workflow)
- Pricing Procedure
- Account Determination
- Source Determination

---

## 2. Cutover 일정 (예시)

| 단계 | 내용 | 담당 |
|------|------|------|
| D-14 | 마스터 데이터 정합성 점검 | MM |
| D-10 | 승인 Workflow 최종 테스트 | MM/Key User |
| D-7  | Condition Record 동결 | MM |
| D-5  | OBYC 계정 매핑 재검증 | MM/FI |
| D-3  | 미처리 PO/GR 정리 | MM |
| D-1  | 시스템 전환 준비 완료 확인 | IT |
| D-Day | Go-Live | 전체 |

---

## 3. 데이터 정합성 점검 항목

- Material Master 필수 View 존재 여부
- Valuation Class 누락 여부
- Info Record 유효기간
- Source List 고정 공급업체 설정
- 승인 전략 조건 테스트 완료 여부

---

## 4. Open Item 정리

### 4.1 미입고 PO
- MB5S 리포트 확인
- 장기 미입고 PO 처리 여부 결정

### 4.2 GR/IR 잔액
- MR11 실행 여부
- 잔액 30일 초과 항목 점검

### 4.3 송장 블로킹
- MRBR 점검
- 불필요 블록 해제

---

## 5. 리스크 관리

| 리스크 | 대응 방안 |
|--------|------------|
| 승인 지연 | Workflow Agent 재확인 |
| 가격 오류 | Pricing Procedure 긴급 점검 |
| 회계 전표 오류 | OBYC 재검증 |
| 대량 오류 발생 | 긴급 롤백 전략 준비 |

---

## 6. 롤백 전략

- 기존 승인 전략 백업 유지
- Pricing Schema 이전 버전 보관
- Condition Record 백업 데이터 확보
- 긴급 승인 임시 우회 프로세스 준비

---

## 7. Go-Live 이후 모니터링

- 1주차: 일일 리포트 점검
- 2주차: GR/IR 잔액 집중 관리
- 1개월: KPI 기반 안정화 평가

---

## 8. 성공 기준

- 승인 평균 처리 시간 30% 감소
- 가격 오류 발생률 감소
- GR/IR 잔액 감소
- 사용자 만족도 개선

---

## 9. 컨설턴트 역할

- Cutover 일정 수립
- 데이터 정합성 검증
- Key User 지원
- 초기 오류 대응 및 안정화 지원
