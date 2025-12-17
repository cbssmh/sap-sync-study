# ABAP Authority Check

- 사용자 권한을 확인하는 보안 기능
- 권한 없으면 기능 실행 불가

## Authority Object
- 권한 체크 단위
- Role을 통해 사용자에게 부여됨

## 기본 문법
AUTHORITY-CHECK OBJECT 'M_BEST_EKG'
  ID 'EKGRP' FIELD lv_ekgrp
  ID 'ACTVT' FIELD '03'.

## 결과 확인
- sy-subrc = 0  : 권한 있음
- sy-subrc ≠ 0 : 권한 없음

## ACTVT 값
- 01 생성
- 02 변경
- 03 조회
- 06 삭제
