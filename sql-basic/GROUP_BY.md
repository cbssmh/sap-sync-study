# SQL GROUP BY 정리

## 1. GROUP BY 개념
- 데이터를 특정 기준(컬럼)으로 묶어서 집계할 때 사용
- SUM, COUNT, AVG, MAX, MIN 등 집계 함수와 함께 사용

## 2. 기본 형태
SELECT 컬럼, 집계함수  
FROM 테이블명  
GROUP BY 컬럼;

## 3. 예시 1: 카테고리별 상품 개수 출력
SELECT category, COUNT(*)  
FROM products  
GROUP BY category;

## 4. 예시 2: 부서별 평균 급여
SELECT department, AVG(salary)  
FROM employees  
GROUP BY department;

## 5. HAVING 절 (조건 추가)
- GROUP BY 이후 결과에 조건을 걸 때 사용

예시:
SELECT category, COUNT(*)  
FROM products  
GROUP BY category  
HAVING COUNT(*) > 5;

## 6. GROUP BY 사용할 때 주의사항
- SELECT 절에 쓰는 컬럼은 반드시 GROUP BY에도 포함되어야 함
- 집계 함수는 GROUP BY와 함께 쓰는 것이 기본
