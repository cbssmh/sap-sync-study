# [프로젝트 시뮬레이션] Customizing 설계 문서

## 1. 설계 개요

프로젝트명:
- 구매 프로세스 표준화 및 승인 자동화

목표:
- 승인 자동화
- 가격 통제 강화
- 회계 오류 최소화

---

## 2. 조직 구조 설정

### Company Code
- 1000

### Plant
- 1000 (Main Plant)

### Purchasing Organization
- 1000

### Purchasing Group
- A01

설정 경로:
SPRO → Enterprise Structure → Materials Management

---

## 3. 승인 프로세스 설정

### Flexible Workflow 적용

조건:
- Net Amount ≤ 10,000 → 자동 승인
- 10,000 < Net Amount ≤ 50,000 → 팀장 승인
- > 50,000 → 2단계 승인

설정 경로:
SPRO → Flexible Workflow
또는 Fiori: Manage Workflows for Purchase Orders

---

## 4. 가격 결정 설정

### Pricing Procedure
- ZMM_STD

구성:
- Step 10: PB00 (기본 가격)
- Step 20: RA01 (할인)
- Step 30: FRA1 (운임)

Access Sequence:
- Vendor + Material 우선

설정 경로:
SPRO → MM → Purchasing → Conditions

---

## 5. 계정 결정 (OBYC)

Transaction Keys:
- BSX → 재고 계정 140000
- WRX → GR/IR 계정 200000
- GBB → 소비 계정 500000
- PRD → 가격 차이 계정 510000

Valuation Class:
- 3000 (Finished Goods)

설정 경로:
SPRO → MM → Valuation → OBYC

---

## 6. Source Determination

- Source List 필수화
- Fixed Vendor 지정
- Info Record 유효기간 관리

설정 경로:
SPRO → MM → Purchasing → Source List

---

## 7. 재고 및 실사 설정

- Physical Inventory 연 1회 + Cycle Counting
- Movement Type 101/102 표준화

---

## 8. 테스트 전략

- 단위 테스트 (UT)
- 통합 테스트 (SIT)
- 사용자 승인 테스트 (UAT)

---

## 9. 리스크 및 대응

| 리스크 | 대응 방안 |
|--------|------------|
| 승인 지연 | Workflow 로그 모니터링 |
| 가격 오류 | Condition Record 주기 점검 |
| GR/IR 잔액 | 월말 정리 프로세스 운영 |

---

## 10. 결론

본 설계는 승인 간소화와 가격 통제 강화를 중심으로,
MM–FI 통합 안정성을 확보하는 것을 목표로 한다.
