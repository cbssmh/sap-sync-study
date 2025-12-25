# ABAP SELECT 성능 기본 정리

## 1. SELECT 성능이 중요한 이유
- SAP 성능 이슈의 대부분이 SELECT에서 발생
- 대량 데이터 조회 시 사용자 체감 속도에 직접 영향

---

## 2. 기본 원칙
- 필요한 필드만 조회 (SELECT *)
- WHERE 조건 필수 사용
- 가능한 한 DB에서 필터링

---

## 3. SELECT * 지양
- 불필요한 컬럼까지 모두 조회
- 네트워크/메모리 낭비 발생

권장:
SELECT matnr, mtart
  FROM mara
  INTO TABLE @DATA(lt_mara).

---

## 4. WHERE 조건 사용
- 조건 없는 SELECT는 전체 테이블 스캔 유발
- Key 필드 조건 우선 사용

예)
SELECT *
  FROM ekko
  INTO TABLE @DATA(lt_ekko)
 WHERE bukrs = '1000'.

---

## 5. LOOP 안에서 SELECT 금지
- N+1 문제 발생
- 성능 급격히 저하

나쁜 예:
LOOP AT lt_mat INTO ls_mat.
  SELECT * FROM mara INTO ls_mara WHERE matnr = ls_mat-matnr.
ENDLOOP.

---

## 6. JOIN 활용
- 여러 SELECT 대신 JOIN으로 한 번에 조회
- DB에서 처리 → 성능 향상

---

## 7. 실무 포인트
- 느리면 ST05(SQL Trace) 의심
- 조회 조건/범위부터 점검
- 컨설턴트도 SELECT 구조는 읽을 수 있어야 함