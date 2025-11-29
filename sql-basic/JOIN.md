# SQL JOIN 정리

## 1. JOIN 개념
- 여러 테이블을 연결해서 하나의 결과로 조회하는 방식
- 관계형 데이터베이스에서 매우 중요함
- SAP 같은 ERP 시스템에서도 테이블 JOIN이 기본

## 2. INNER JOIN
- 두 테이블에서 "조건이 일치하는" 데이터만 조회

예시:
SELECT *
FROM orders o
INNER JOIN customers c
  ON o.customer_id = c.id;

## 3. LEFT JOIN
- 왼쪽 테이블은 모두 가져오고,
- 오른쪽 테이블은 조건이 맞는 것만 가져옴

예시:
SELECT *
FROM products p
LEFT JOIN categories c
  ON p.category_id = c.id;

## 4. RIGHT JOIN
- 오른쪽 테이블을 모두 표현하고,
- 왼쪽은 조건 맞는 것만

예시:
SELECT *
FROM employees e
RIGHT JOIN departments d
  ON e.dept_id = d.id;

## 5. JOIN 사용 포인트
- PK/FK 관계 기반으로 Join
- 테이블 alias(o, c, p 같은 단축이름) 자주 사용
- INNER JOIN이 가장 기본
