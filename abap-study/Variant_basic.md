# ABAP Variant 기본 정리

## 1. Variant란?
- Report Program의 Selection Screen 값을 저장한 설정값
- 동일 프로그램을 조건만 바꿔 반복 실행할 때 사용

---

## 2. Variant 사용 목적
- 매번 조건 입력하는 번거로움 제거
- Batch Job에서 필수적으로 사용
- 사용자 실수(조건 오입력) 방지

---

## 3. Variant 구성 요소
- Selection Screen 입력값
- 선택/미선택 옵션
- 기본값(Default) 설정 가능

---

## 4. Variant 생성/관리
- 실행 화면에서 Variant 저장
- 트랜잭션: SE38 / SA38
- 개인용 / 공용 Variant 구분

---

## 5. Batch Job과의 관계
- Batch Job 실행 시 Variant 지정
- 동일 프로그램 + 다른 Variant로 여러 Job 구성 가능

---

## 6. 실무 포인트
- 대량 조회 Report는 반드시 Variant와 함께 사용
- 공용 Variant 변경 시 영향 범위 확인 필요
- 컨설턴트는 “어떤 Variant로 실행했는지”부터 확인
