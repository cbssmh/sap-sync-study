# ABAP Internal Table 예제

## 1) Internal Table 선언 + 데이터 추가

DATA: lt_num TYPE TABLE OF i,
      lv_num TYPE i.

lv_num = 10.
APPEND lv_num TO lt_num.

lv_num = 20.
APPEND lv_num TO lt_num.


## 2) LOOP로 Internal Table 읽기

LOOP AT lt_num INTO lv_num.
  WRITE: / 'VALUE =', lv_num.
ENDLOOP.


## 3) 구조체 + 테이블 선언 예제

TYPES: BEGIN OF ty_mat,
         matnr TYPE mara-matnr,
         mtart TYPE mara-mtart,
       END OF ty_mat.

DATA: lt_mat TYPE TABLE OF ty_mat,
      ls_mat TYPE ty_mat.

ls_mat-matnr = 'A0001'.
ls_mat-mtart = 'FERT'.
APPEND ls_mat TO lt_mat.


## 4) READ TABLE으로 특정 행 읽기

READ TABLE lt_mat INTO ls_mat
     WITH KEY matnr = 'A0001'.

IF sy-subrc = 0.
  WRITE: / 'Found:', ls_mat-matnr, ls_mat-mtart.
ENDIF.
