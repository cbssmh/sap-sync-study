# ABAP SELECT 예제

## 1) 단일 조건
SELECT *
  FROM mara
  INTO TABLE @DATA(lt_mara)
 WHERE matnr = 'A0001'.

## 2) 조건 + 정렬
SELECT matnr, maktx
  FROM makt
  INTO TABLE @DATA(lt_makt)
 WHERE spras = 'EN'
 ORDER BY matnr ASC.

## 3) JOIN 예제 (EKKO + EKPO)
SELECT a~ebeln, a~bukrs, b~matnr, b~menge
  FROM ekko AS a
  INNER JOIN ekpo AS b
    ON a~ebeln = b~ebeln
  INTO TABLE @DATA(lt_result)
 WHERE a~bukrs = '1000'.
