# SQL 집계 함수 (Aggregate Functions) 정리

## 1. 집계 함수란?
- 여러 행(row)의 값을 하나의 결과로 요약하는 함수
- GROUP BY와 함께 자주 사용됨
- SAP·ERP 같은 시스템에서도 데이터 분석 시 매우 중요

## 2. 주요 집계 함수

### ✔ COUNT()
- 행의 개수를 셈
예시:
SELECT COUNT(*) FROM users;

### ✔ SUM()
- 숫자 컬럼의 총합
예시:
SELECT SUM(price) FROM orders;

### ✔ AVG()
- 평균값 계산
예시:
SELECT AVG(salary) FROM employees;

### ✔ MAX()
- 가장 큰 값
예시:
SELECT MAX(score) FROM exams;

### ✔ MIN()
- 가장 작은 값
예시:
SELECT MIN(stock) FROM products;

## 3. GROUP BY와 함께 쓰는 예시
SELECT department, AVG(salary)
FROM employees
GROUP BY department;

## 4. WHERE와 함께 쓰는 예시
SELECT COUNT(*)
FROM orders
WHERE status = 'DONE';

## 5. 주의사항
- SELECT 절에서 집계함수와 일반 컬럼을 함께 쓰면 → GROUP BY 필요
- 문자열 컬럼에는 SUM/AVG 사용 불가
