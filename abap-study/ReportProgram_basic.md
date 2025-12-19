# ABAP Report Program 기본 정리

## 1. Report Program이란?
- ABAP에서 데이터를 조회하여 화면(List/ALV)으로 출력하는 프로그램
- Z Report 형태로 가장 많이 개발됨
- 조회용, 집계용, 현업 리포트에 주로 사용

---

## 2. Report Program 기본 구조
- REPORT 문으로 시작
- 선언부 → 이벤트 → 처리 로직 순서

예)
REPORT zsample_report.

---

## 3. 주요 이벤트(Event)

### START-OF-SELECTION
- Report Program의 메인 로직 시작 지점
- 대부분의 SELECT 문이 여기서 실행됨

### END-OF-SELECTION
- 데이터 조회가 끝난 후 출력 처리
- ALV 출력 위치로 자주 사용

---

## 4. Selection Screen
- 사용자가 조회 조건을 입력하는 화면
- PARAMETERS / SELECT-OPTIONS 사용

예)
PARAMETERS: p_bukrs TYPE bukrs.
SELECT-OPTIONS: s_matnr FOR mara-matnr.

---

## 5. 기본 처리 흐름
1) Selection Screen에서 조건 입력
2) START-OF-SELECTION에서 데이터 조회
3) Internal Table에 데이터 저장
4) END-OF-SELECTION에서 출력(ALV/List)

---

## 6. Report Program vs Module Pool
- Report Program  
  · 조회 중심  
  · 단순 구조  
  · 대부분 ALV 출력

- Module Pool  
  · 화면(Screen) 중심  
  · 버튼, 입력 처리  
  · 트랜잭션 프로그램

---

## 7. 실무 포인트
- MM/FI/SD 조회 프로그램은 거의 Report Program
- 성능 이슈 시 SELECT 구조가 가장 중요
- 컨설턴트는 “조회 조건 → 결과 흐름”을 설명할 수 있어야 함
