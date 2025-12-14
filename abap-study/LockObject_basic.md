# ABAP Lock Object 기초 정리

## 1) Lock Object란?
- SAP에서 동일 데이터에 대한 동시 수정(Concurrency)을 막기 위한 기능
- 여러 사용자가 동시에 같은 데이터를 변경하는 것을 방지함

---

## 2) 왜 Lock이 필요한가?
- 두 사용자가 동시에 같은 PO를 수정하는 상황 방지
- 데이터 불일치, 덮어쓰기 오류 예방
- MM 실무에서 매우 자주 발생하는 이슈 포인트

---

## 3) Lock Object 동작 방식
- ENQUEUE : 데이터 잠금
- DEQUEUE : 데이터 잠금 해제
- SAP 시스템 레벨에서 관리됨

---

## 4) Lock Object 사용 흐름
1. 데이터 수정 전 ENQUEUE 호출
2. 수정 작업 수행
3. 작업 완료 후 DEQUEUE 호출

---

## 5) ABAP 코드 예시 (개념용)

ENQUEUE_EZ_PO
  EXPORTING
    ebeln = lv_ebeln.

" 데이터 처리 로직

DEQUEUE_EZ_PO
  EXPORTING
    ebeln = lv_ebeln.

---

## 6) Lock 실패 시
- 이미 다른 사용자가 Lock을 잡고 있으면 Lock 실패
- 사용자에게 메시지 표시 필요
- 잠시 후 재시도 유도

---

## 7) MM 컨설턴트에게 중요한 이유
- PO, GR, IV 오류 원인 분석 시 Lock 여부 확인 필수
- 사용자 불만의 원인이 Lock 충돌인 경우 많음
- 개발자에게 정확한 조치 요청 가능
