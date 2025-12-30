# ABAP 오류 처리 기본 (SY-SUBRC / MESSAGE)

## 1. 오류 처리란?
- 프로그램 실행 중 발생하는 예외 상황을 감지하고 대응하는 로직
- 사용자 오류 안내 및 프로그램 안정성 확보 목적

---

## 2. SY-SUBRC
- ABAP 명령 실행 결과를 저장하는 시스템 변수
- 0이면 성공, 0이 아니면 실패

예)
READ TABLE lt_data INTO ls_data WITH KEY id = lv_id.
IF sy-subrc <> 0.
  MESSAGE '데이터가 없습니다.' TYPE 'E'.
ENDIF.

---

## 3. SELECT 결과 확인
- SELECT 후 반드시 결과 존재 여부 확인 필요

예)
SELECT * FROM mara INTO TABLE lt_mara WHERE mtart = 'FERT'.
IF sy-subrc <> 0.
  MESSAGE '조회 결과 없음' TYPE 'I'.
ENDIF.

---

## 4. MESSAGE 유형
- I : Information (정보)
- S : Success (성공)
- W : Warning (경고)
- E : Error (오류, 처리 중단)
- A : Abort (강제 종료)

---

## 5. MESSAGE 사용 시 주의
- TYPE 'E'는 화면 이동을 막음
- 반복 메시지는 사용자 불편 유발
- 오류 원인을 명확히 안내해야 함

---

## 6. 실무 포인트
- 오류 발생 지점에서 즉시 메시지 처리
- 사용자 입력 오류 vs 시스템 오류 구분
- 컨설턴트는 “왜 이 오류가 발생했는지” 설명 가능해야 함
