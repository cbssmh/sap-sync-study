# ABAP Batch Job 기본 정리

## 1. Batch Job이란?
- 사용자의 직접 실행 없이 백그라운드에서 자동 실행되는 작업
- 대량 처리, 정기 처리, 야간 배치에 사용

---

## 2. Batch Job 사용 목적
- 업무 시간 외 대량 데이터 처리
- 반복 작업 자동화
- 사용자 화면 성능 영향 최소화

---

## 3. Batch Job 구성 요소
- Job Name : 작업 식별 이름
- Job Step : 실행할 프로그램(Report)
- Variant : 실행 조건(Selection Screen 값)
- Start Condition : 실행 시점(즉시/예약)

---

## 4. Batch Job 생성 흐름
1) 실행할 Report Program 준비
2) Variant 생성 (조회 조건 저장)
3) Job 생성 및 Step 연결
4) 실행 시점 설정
5) Job 실행 및 로그 확인

---

## 5. 주요 트랜잭션
- SM36 : Job 생성
- SM37 : Job 모니터링/로그 확인

---

## 6. 실무 포인트
- 대량 조회/처리는 Batch Job으로 분리
- 실패 Job은 SM37에서 원인 분석
- 권한 부족으로 Job 실패하는 경우 많음
- 컨설턴트는 “왜 배치로 돌리는지” 설명 가능해야 함
