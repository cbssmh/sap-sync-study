# ABAP 기본 개념 정리

## 1. ABAP이란?
SAP에서 사용하는 언어.  
데이터 조회(SELECT), 내부 테이블 처리, 보고서 프로그램 등에 사용됨.

## 2. 기본 문법 예시
REPORT zsample.

DATA lv_text TYPE string.
lv_text = 'Hello ABAP'.
WRITE: / lv_text.

## 3. Internal Table & Work Area
- Internal Table: 여러 행을 담는 SAP의 리스트 구조
- Work Area: 테이블의 한 행(한 줄)

예시:
DATA: lt_mara TYPE TABLE OF mara,
      ls_mara TYPE mara.

## 4. SELECT 기본 형태
SELECT *
  FROM mara
  INTO TABLE lt_mara.

조건 추가:
SELECT *
  FROM ekko
  INTO TABLE lt_ekko
 WHERE bukrs = '1000'.

## 5. LOOP로 테이블 읽기
LOOP AT lt_mara INTO ls_mara.
  WRITE: / ls_mara-matnr.
ENDLOOP.

## 6. 컨설턴트가 ABAP을 알아야 하는 이유
- 오류 분석 시 테이블 구조 파악
- 개발자와 협업할 때 의사소통 쉬움
- 실무에서 요구사항 문서(RICEF) 작성에 도움
