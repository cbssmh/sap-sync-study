# SAP MM Project Simulation – Interview Summary

## 1. 프로젝트 개요

목표  
- 구매 프로세스 표준화  
- 승인 자동화  
- 가격 오류 감소  
- MM–FI 통합 안정성 확보  

범위  
PR → PO → GR → IR → FI Posting

---

## 2. 주요 문제점 (As-Is)

프로젝트 시뮬레이션에서 가정한 주요 문제

- 승인 단계 과다로 구매 리드타임 증가
- Info Record 미관리로 가격 오류 발생
- GR/IR 잔액 장기 미정리
- 승인 이후 가격 변경 통제 미흡

---

## 3. To-Be 설계

### 승인 프로세스 개선

Flexible Workflow 도입

조건 예

- ≤ 10,000 : 자동 승인
- 10,000 ~ 50,000 : 팀장 승인
- > 50,000 : 부서장 승인

효과  
승인 리드타임 단축

---

### 가격 통제 강화

적용 설정

- Info Record 필수화
- Pricing Procedure 검증
- 승인 이후 가격 변경 시 재승인

---

### 계정결정 안정화

OBYC 설정 검증

핵심 Transaction Key

- BSX : Inventory
- WRX : GR/IR
- GBB : Consumption
- PRD : Price Difference

---

## 4. End-to-End 흐름 검증

테스트 시나리오

PR 생성  
→ 승인  
→ PO 생성  
→ GR (101)  
→ IR (MIRO)  
→ FI 전표 확인

검증 포인트

- 가격 정상 계산
- GR/IR 상계
- Accounting Document 자동 생성

---

## 5. 주요 학습 성과

이 프로젝트 시뮬레이션을 통해

- MM End-to-End 프로세스 이해
- OBYC 기반 계정결정 구조 이해
- Pricing Procedure 동작 이해
- 승인 전략 설계 경험
- MM–FI 통합 흐름 분석

---

## 6. 면접용 답변 구조

질문:  
"프로젝트에서 어떤 역할을 했나요?"

답변 구조

1. 구매 프로세스 문제 분석  
2. 승인 및 가격 통제 설계  
3. OBYC 계정결정 검증  
4. End-to-End 테스트 수행  
5. 프로세스 개선 효과 설명

---

## 7. 프로젝트 핵심 포인트

- 프로세스 중심 설계
- 설정(Customizing) 이해
- 회계 통합 구조 분석
- 오류 발생 원인 추적 가능
