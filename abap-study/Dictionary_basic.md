# ABAP Dictionary 기본 정리

ABAP Dictionary(DDIC)는 SAP의 데이터 구조를 정의하는 영역.
테이블, 도메인, 데이터 요소 등을 관리하는 곳.

---

## 1) Domain (도메인)
- 필드의 기술적 속성을 정의
- 예: 길이, 데이터 타입(Char, Num, Date 등)

예)
MATNR의 Domain: MATNR  
타입: CHAR  
길이: 18


## 2) Data Element (데이터 요소)
- 필드의 의미적 속성을 정의
- 설명 텍스트, 필드 라벨 등이 여기서 결정됨
- 테이블의 각 필드는 Domain + Data Element로 구성됨

예)
EKKO-EBELN (구매오더 번호)의 Data Element: EBELN


## 3) Table (테이블)
SAP의 실제 데이터가 저장되는 DB 구조.

### 테이블 구성
- **필드(Field)**  
- **Primary Key(기본키)**  
- **Data Element / Domain**  
- **Technical settings**

예)
MARA: 자재 기본 데이터(자재코드, 자재그룹 등)  
EKKO: 구매오더 헤더 정보  
EKPO: 구매오더 아이템 정보


## 4) Structure (구조체)
- 실제 데이터 저장용 X  
- 프로그램에서 데이터를 담기 위한 타입 정의  
- 여러 테이블의 필드를 묶어서 사용할 때 편리

예)
TY_MARA 구조체 만들어서 Internal Table에 사용 가능


## 5) Table Type
- Internal Table의 “타입”을 정의하는 오브젝트
- 반복적으로 쓸 테이블 구조를 표준화할 때 사용


## 6) View (뷰)
- 여러 테이블을 조인해 하나처럼 보여주는 논리적 객체
- 실제 저장 공간 없음 (논리적 조회 전용)

예)
MATDOC_ALLVIEW 같은 통합 조회용 뷰


## 7) 컨설턴트가 DDIC를 알아야 하는 이유
- 테이블/필드 구조를 이해해야 오류 분석 가능  
- 개발자와 테이블 기반 요청 주고받을 때 필수 지식  
- MM 실무에서 MARA, MARC, EKKO, EKPO 등 DDIC 테이블 이해도가 매우 중요  
- 보고서 요구사항(RICEF) 작성 시 필드 단위 파악 가능
