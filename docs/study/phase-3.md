# Phase 3: 사내 자동화와 행동 제어 (Enterprise Automation)

실제 사내 시스템(SAP, dataPARC)과 연동하고, AI의 실수를 사람이 바로잡는 안전장치를 만듭니다.

---

## 6주차: 도구 제작과 시스템 연동 1 (SAP)

* **학습 목표:** 폐쇄적인 사내 시스템(SAP)을 AI가 조회할 수 있도록 API/Wrapper 씌우기
* **핵심 키워드:** `Agent Middleware`, `SAP 연동`, `Function Calling`
* **실습:**
    * **자재 조회 에이전트:** "A 부품 재고 있어?" → SAP RFC/BAPI 호출 도구 실행 → 재고 수량 답변 (보안상 Read-only부터 시작)

---

## 7주차: 도구 제작과 시스템 연동 2 (dataPARC)

* **학습 목표:** 공정 데이터 시스템(dataPARC) 조회 및 시각화
* **핵심 키워드:** `dataPARC`, `Context Engineering` (데이터 해석 프롬프트)
* **실습:**
    * **공정 이상 감지 리포터:** dataPARC 태그 값 조회 → 최근 1시간 데이터 추이 분석 → 이상 징후 시 코멘트 작성

---

## 8주차: 인간 개입과 가드레일 (Safety & Control)

* **학습 목표:** AI가 멋대로 행동(Write/Delete)하지 못하게 승인 절차 추가
* **핵심 키워드:** `HITL (Human-in-the-Loop)`, `가드레일(Guardrails)`, `체크포인트`
* **실습:**
    * **구매 요청 승인 봇:** 사용자 요청(SAP 구매 생성) → AI가 내용 작성 후 `interrupt` → 관리자(사람)가 승인 버튼 클릭 → 실제 SAP 전송
