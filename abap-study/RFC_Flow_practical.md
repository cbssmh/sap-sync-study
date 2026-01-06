# ABAP RFC 실전 흐름 정리

## 1. RFC 실전에서 언제 쓰나?
- SAP ↔ 외부 시스템 실시간 연동
- SAP ↔ SAP 시스템 간 데이터 교환
- 인터페이스 오류/지연 이슈 대응

---

## 2. RFC 기본 흐름
1) 송신 시스템에서 Function Module 호출
2) RFC Destination으로 대상 시스템 지정
3) 대상 시스템에서 Function Module 실행
4) 결과(Return/Exception) 수신

---

## 3. RFC Function Module 구조
- Importing : 입력 값
- Exporting : 출력 값
- Tables    : 대량 데이터
- Exceptions: 오류 처리

---

## 4. 호출 예시 (개념)
CALL FUNCTION 'Z_RFC_SAMPLE'
  DESTINATION 'RFC_DEST'
  EXPORTING
    iv_key = lv_key
  IMPORTING
    ev_result = lv_result
  EXCEPTIONS
    system_failure        = 1
    communication_failure = 2.

IF sy-subrc <> 0.
  MESSAGE 'RFC 호출 오류' TYPE 'E'.
ENDIF.

---

## 5. 오류 유형
- Communication Failure : 네트워크/연결 문제
- System Failure       : 대상 시스템 오류
- Authorization Error  : 권한 문제

---

## 6. 실무 포인트
- RFC Destination 설정(SM59) 확인 필수
- 타임아웃/재시도 정책 중요
- 오류 발생 시 로그 + sy-subrc 함께 확인
- 컨설턴트는 “어디에서 끊겼는지” 흐름 설명 가능해야 함
