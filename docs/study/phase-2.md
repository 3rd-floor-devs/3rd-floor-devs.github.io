# Phase 2: 에이전트의 귀와 기억 (상호작용 & RAG)

에이전트가 사용자와 음성으로 소통하고, 과거의 기억(데이터)을 활용하도록 업그레이드합니다.

---

## 4주차: 말하는 에이전트 (The Speaker - Speech)

* **학습 목표:** 텍스트 기반 봇을 음성 인터페이스로 확장 (멀티모달 UX)
* **핵심 키워드:** `STT/TTS` (OpenAI Whisper or Azure Speech), `Tool 적용`
* **실습 [Speech + Tools]:**
    * **음성 비서:** 음성 명령("저 이미지 분석해줘") → STT → LangGraph 실행(Vision 도구 호출) → 결과 요약 → TTS로 음성 답변

---

## 5주차: 기억하는 에이전트 (The Brain - RAG & Memory)

* **학습 목표:** 단기 대화 기억과 장기 문서 지식을 구분하여 저장하고 검색하기
* **핵심 키워드:** `RAG`, `Long/Short 메모리`, `Vector Store`
* **실습:**
    * **사내 매뉴얼 Q&A:** 사내 규정 PDF(OCR 처리됨)를 기반으로 답변하되, 이전 대화 맥락(Short Memory)을 기억하며 답변하는 봇
