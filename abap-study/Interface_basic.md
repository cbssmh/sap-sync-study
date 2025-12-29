# ABAP 인터페이스 기본 (IDoc / RFC)

## 1. 인터페이스란?
- SAP와 외부 시스템(또는 SAP 내부 시스템) 간 데이터 교환 방식
- 실무에서 매우 빈번하게 사용

---

## 2. RFC (Remote Function Call)
- SAP 간 또는 SAP ↔ 외부 시스템 간 함수 호출 방식
- 실시간 처리에 적합

특징:
- 동기/비동기 호출 가능
- Function Module 기반
- 오류 시 즉시 확인 가능

주요 유형:
- Synchronous RFC
- Asynchronous RFC
- Transactional RFC (tRFC)
- Queued RFC (qRFC)

---

## 3. IDoc (Intermediate Document)
- 메시지 기반 데이터 교환 방식
- 대량 데이터, 비동기 처리에 적합

특징:
- 구조화된 문서 형태
- 송신 → 수신 단계 분리
- 오류 발생 시 재처리 가능

구성:
- Control Record
- Data Record
- Status Record

---

## 4. RFC vs IDoc 비교
- RFC:
  · 실시간
  · 빠른 응답
  · 소량 데이터

- IDoc:
  · 비동기
  · 대량 처리
  · 안정성/재처리 강점

---

## 5. 실무 포인트
- 실시간 연동 요구 → RFC
- 대량/야간 배치 → IDoc
- 오류 문의 시 인터페이스 유형부터 확인
- 컨설턴트는 흐름(송신/수신)을 설명할 수 있어야 함
