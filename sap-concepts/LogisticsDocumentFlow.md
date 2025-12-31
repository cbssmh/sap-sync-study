# SAP MM 물류 문서 흐름 (Material / Accounting Document)

## 1. 물류 문서 흐름이란?
- 자재 이동 시 생성되는 문서들의 연결 관계
- 수량(물류)과 금액(회계)을 함께 추적하는 구조

---

## 2. Material Document (자재 문서)
- 자재의 입고/출고/이동 시 생성
- 수량 변화의 근거 문서

주요 특징:
- Movement Type 포함 (101, 261 등)
- Plant / Storage Location 기준
- 대표 테이블: MKPF(헤더), MSEG(아이템)

---

## 3. Accounting Document (회계 문서)
- 재고 변동에 따른 금액 변화를 기록
- FI 모듈로 자동 생성

주요 특징:
- 차변/대변 계정 생성
- 금액 기준 문서
- 대표 테이블: BKPF(헤더), BSEG(아이템)

---

## 4. 문서 생성 흐름 예시
- PO 생성 (ME21N)
- GR 처리 (MIGO, 101)
  → Material Document 생성
  → Accounting Document 자동 생성

---

## 5. 문서 연결 포인트
- 하나의 자재 이동에 대해
  · Material Document (수량)
  · Accounting Document (금액)
  가 함께 생성됨

---

## 6. 실무 포인트
- 수량 오류 → Material Document 확인
- 금액 오류 → Accounting Document 확인
- Movement Type이 두 문서에 미치는 영향 큼
- 컨설턴트는 “수량 vs 금액”을 구분해서 설명해야 함
