# SAP MM Process Design Portfolio

## 📌 Overview

본 프로젝트는 단순 SAP 개념 학습이 아닌,
**구매 프로세스(PR → PO → GR → IR)를 실제 기업 상황 기반으로 재설계하고,
MM–FI 통합까지 고려한 프로세스 설계 능력을 검증하기 위한 포트폴리오**입니다.

---

## 🎯 Problem Statement

기존 구매 프로세스의 주요 문제:

* 승인 지연으로 인한 구매 리드타임 증가
* 가격 통제 부재
* GR/IR 불일치로 인한 회계 정합성 문제

---

## 🛠 Solution

다음과 같은 방식으로 프로세스를 재설계:

* Flexible Workflow 기반 자동 승인
* Price Control 전략 적용
* MM–FI 통합 기반 자동 전표 처리

---

## 🔄 End-to-End Flow

PR → PO → GR → IR → FI Posting

* 구매 요청 생성
* 승인 자동화
* 입고 처리
* 송장 검증
* 회계 전표 자동 생성

---

## 💡 Key Design Decisions

* Flexible Workflow 선택 (기존 Release Strategy 대체)
* Price Control S 사용
* OBYC 기반 자동 계정 결정 설계

---

## 📊 Outcome

* 승인 시간 단축
* 회계 오류 감소
* 프로세스 자동화율 증가

---

## 📁 Key Documents

* [To-Be Process](./03_to_be_design/to_be_process.md)
* [MM-FI Integration](./04_mm_fi_integration/end_to_end_flow.md)
* [Design Decisions](./03_to_be_design/design_decisions.md)

---

## 🚀 What I Learned

* SAP MM 프로세스의 End-to-End 흐름 이해
* MM–FI 통합 구조 설계 경험
* 비즈니스 요구사항을 시스템으로 변환하는 능력 강화
