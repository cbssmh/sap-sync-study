# SAP MM Release Strategy 설정 단계 상세 정리 (Classic)

## 1. 설정 개요
- PO 승인 전략을 조건 기반으로 설정
- 금액, 구매조직, 문서 유형 등을 기준으로 승인 흐름 결정

---

## 2. 전체 설정 흐름

1) Release Group 생성
2) Release Code 생성
3) Release Indicator 정의
4) Strategy 정의
5) Classification 연결

---

## 3. 단계별 상세

### ① Release Group 정의

SPRO
→ MM
→ Purchasing
→ PO
→ Release Procedure for Purchase Orders
→ Define Release Groups

- 문서 유형(Document Type)과 연결

---

### ② Release Code 정의

- 승인자 코드 생성 (예: A1, B1)
- 승인 단계별 담당자 지정

주의:
- Role/권한 오브젝트와 연결 필요

---

### ③ Release Indicator 정의

- 승인 전/후 상태 정의
- 승인 완료 시 후속 문서 허용 여부 설정

예:
- 승인 완료 전 PO 변경 가능 여부
- 출력 가능 여부

---

### ④ Release Strategy 정의

- Release Group 내 전략 생성
- 승인 단계 순서 지정
- 승인 코드 연결

---

### ⑤ Classification 설정 (핵심)

경로:
SPRO → Cross-Application Components
→ Classification System

- Class Type: 032 (PO)
- 승인 조건 특성 생성
  · 총 금액
  · 구매조직
  · 문서 유형

- Strategy와 특성 값 매핑

---

## 4. 실제 승인 조건 예시

조건:
- 금액 10,000 초과 시 2단계 승인
- 구매조직 1000 전용 전략

흐름:
1) PO 생성
2) 시스템이 Classification 값 평가
3) 해당 Strategy 결정
4) Release Code 순서대로 승인

---

## 5. 실무에서 가장 많이 틀리는 부분

- Classification 값 미연결
- 금액 조건 범위 설정 오류
- 승인자 권한 누락
- Changeability Indicator 미설정

---

## 6. 면접 대비 핵심 포인트

질문:
"Release Strategy 설정 단계 설명해보세요."

답변 구조:
1) SPRO 경로
2) Release Group / Code / Indicator 설명
3) Classification이 핵심이라고 강조
4) 조건 기반 동작 흐름 설명
