# ABAP Background RFC (tRFC / qRFC) 기본 정리

## 1. Background RFC란?
- 비동기 방식으로 RFC를 실행하는 구조
- 네트워크 지연/오류에 대비해 안정적인 데이터 전달 목적

---

## 2. tRFC (Transactional RFC)
- 트랜잭션 보장 RFC
- 실패 시 자동 재시도
- 호출 순서 보장 X

특징:
- Exactly Once 실행 보장
- 대량 데이터 처리에 적합

---

## 3. qRFC (Queued RFC)
- tRFC + 실행 순서 보장
- 큐(Queue)를 사용해 순차 처리

특징:
- 순서 중요할 때 사용
- 송신/수신 큐 관리 필요

---

## 4. tRFC vs qRFC 비교
- tRFC:
  · 안정성
  · 순서 보장 X
  · 성능 우수

- qRFC:
  · 안정성
  · 순서 보장 O
  · 큐 관리 필요

---

## 5. 주요 관리 트랜잭션
- SM58 : tRFC 모니터링
- SMQ1 : Outbound Queue
- SMQ2 : Inbound Queue

---

## 6. 실무 포인트
- 데이터 누락/중복 이슈 시 tRFC 확인
- 순서 꼬임 이슈 시 qRFC 의심
- 큐 정체 시 전체 인터페이스 지연 발생
- 컨설턴트는 “동기/비동기/순서”를 구분해서 설명 가능해야 함
