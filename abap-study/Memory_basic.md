# SAP Memory / ABAP Memory 기본 정리

## 1) Memory란?
- 프로그램 간에 데이터를 임시로 공유하기 위한 공간
- 화면 이동, 프로그램 호출 시 데이터 전달에 사용

---

## 2) SAP Memory
- 사용자 세션(User Session) 단위로 공유되는 메모리
- SET/GET PARAMETER로 사용
- 주로 화면 간 값 전달에 사용

예)
SET PARAMETER ID 'MAT' FIELD lv_matnr.
GET PARAMETER ID 'MAT' FIELD lv_matnr.

---

## 3) ABAP Memory
- 프로그램 단위로 데이터를 공유
- EXPORT / IMPORT 명령어 사용
- 프로그램 호출 간 데이터 전달에 사용

예)
EXPORT lv_value TO MEMORY ID 'ZDATA'.
IMPORT lv_value FROM MEMORY ID 'ZDATA'.

---

## 4) SAP Memory vs ABAP Memory 차이

- SAP Memory  
  · 사용자 세션 기준  
  · 화면 이동 시 유지  
  · PARAMETER ID 사용  

- ABAP Memory  
  · 프로그램 기준  
  · 명시적 EXPORT/IMPORT 필요  
  · 메모리 ID로 관리  

---

## 5) 실무에서 중요한 이유
- 화면 간 데이터 전달 로직 이해
- 디버깅 시 값이 어디서 넘어오는지 파악 가능
- 개발자 요청사항 이해도 향상
- 불필요한 글로벌 변수 사용 방지
