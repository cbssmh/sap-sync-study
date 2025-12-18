# ABAP ALV 기본 정리

## 1. ALV란?
- ALV(ABAP List Viewer)는 데이터를 표(Table) 형태로 출력하는 SAP 표준 방식
- 대량 데이터 조회, 보고서 프로그램에서 필수적으로 사용
- 정렬, 필터, 합계, 레이아웃 저장 기능을 기본 제공

---

## 2. ALV를 사용하는 이유
- WRITE 문 출력보다 훨씬 가독성 높음
- 사용자(현업)가 직접 정렬/필터 가능
- 개발자 추가 작업 없이 표준 기능 제공
- SAP 실무 보고서의 대부분이 ALV 기반

---

## 3. ALV 종류
- **Classic ALV**  
  - 예전 방식  
  - 단순 출력용

- **Grid ALV (CL_GUI_ALV_GRID)**  
  - 가장 많이 사용  
  - 컨테이너 기반  
  - 이벤트 처리 가능 (더블클릭 등)

- **SALV (Simple ALV)**  
  - 코드 간단  
  - 커스터마이징 제한적  
  - 조회 전용 보고서에 적합

---

## 4. Grid ALV 기본 구성 요소
- Internal Table : 출력할 데이터
- Field Catalog : 컬럼 이름, 순서, 속성
- Container : 화면 영역
- ALV Grid Object : 실제 출력 객체

---

## 5. ALV 기본 흐름
1) Internal Table에 데이터 조회 (SELECT)
2) Field Catalog 정의
3) Container 생성
4) ALV Grid 생성
5) 데이터 출력

---

## 6. 실무 포인트
- 조회 프로그램(Z Report)은 거의 ALV 사용
- 사용자 요구사항(엑셀 다운로드, 정렬)은 ALV로 해결
- 컨설턴트는 ALV 구조를 이해해야 개발자와 소통 가능
