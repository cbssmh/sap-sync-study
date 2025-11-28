# SQL ORDER BY 정리

## 1. ORDER BY 개념
- 조회된 결과를 정렬할 때 사용
- 기본 정렬 방향은 오름차순(ASC)
- 내림차순(DESC) 옵션으로 역순 정렬 가능

## 2. 기본 형태
SELECT *  
FROM 테이블명  
ORDER BY 컬럼명 ASC;   -- 오름차순  
ORDER BY 컬럼명 DESC;  -- 내림차순

## 3. 예시
가격을 높은 순으로 정렬:

SELECT product_name, price  
FROM products  
ORDER BY price DESC;

## 4. 다중 정렬
여러 기준으로 정렬 가능

예시:
SELECT name, age, score  
FROM students  
ORDER BY age ASC, score DESC;
