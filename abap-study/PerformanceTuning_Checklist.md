# ABAP 성능 튜닝 체크리스트

## 1. SELECT 기본 원칙
- SELECT * 사용 지양
- 필요한 필드만 조회
- WHERE 조건 필수

---

## 2. LOOP 안에서 SELECT 금지
- N+1 문제 발생
- 대량 데이터에서 성능 급락

대안:
- JOIN 사용
- FOR ALL ENTRIES 활용

---

## 3. Internal Table 사용
- 필요 없는 데이터는 미리 삭제
- READ TABLE WITH KEY 사용
- SORT + BINARY SEARCH 고려

---

## 4. DB 처리 우선
- 필터링은 DB에서 처리
- ABAP LOOP로 후처리 최소화

---

## 5. Index 활용
- WHERE 조건에 Key 필드 사용
- 빈번한 조회 조건은 Index 확인

---

## 6. 성능 분석 도구
- ST05 : SQL Trace
- SAT  : Runtime Analysis
- SM50/SM66 : Work Process 확인

---

## 7. 실무 포인트
- 느리면 SELECT부터 의심
- 조회 조건 범위 축소가 가장 효과적
- 컨설턴트도 성능 원인 설명 가능해야 함
