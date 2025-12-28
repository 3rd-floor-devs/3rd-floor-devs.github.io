# Phase 4: 지휘관 에이전트 (Architecture)

여러 에이전트를 거느리고 복잡한 작업을 처리하는 고급 아키텍처를 다룹니다.

---

## 9주차: 멀티 에이전트와 슈퍼바이저 (The Manager)

* **학습 목표:** 역할이 다른 여러 에이전트(OCR담당, SAP담당, Vision담당)를 관리자가 조율
* **핵심 키워드:** `Supervisor`, `Multi-Agent`, `Agent State Handoff`
* **실습:**
    * **설비 점검 종합 리포터:**
        * 슈퍼바이저: 사용자 명령 분배
        * Vision 에이전트: 설비 사진 분석 (녹슴, 파손 확인)
        * SAP 에이전트: 해당 설비의 지난 정비 이력 조회
        * 최종: 두 정보를 합쳐 "정비 필요 여부" 보고서 작성

---

## 10주차: 확장성과 표준 프로토콜 (Future Proofing)

* **학습 목표:** 다양한 AI 도구와 모델을 표준화된 방식으로 연결
* **핵심 키워드:** `MCP (Model Context Protocol)`, `Custom Tool Server`
* **실습:**
    * MCP 서버를 구축하여 로컬 파일 시스템이나 사내 DB를 안전하게 에이전트에 연결해보기
