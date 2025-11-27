# SQL WHERE 조건절 정리

## 1. WHERE 개념
- 특정 조건을 만족하는 데이터만 조회할 때 사용
- SELECT와 함께 쓰임

## 2. 기본 형태
SELECT *  
FROM 테이블명  
WHERE 조건;

## 3. 예시
SELECT *  
FROM users  
WHERE age >= 20;

## 4. 복합 조건
- AND: 모두 만족해야 함  
- OR: 하나만 만족해도 됨

예시:
SELECT *  
FROM products  
WHERE price > 10000 AND stock > 0;
