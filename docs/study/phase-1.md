# Phase 1: 에이전트의 뇌와 눈을 만들다 (기초 & 인식)

이 단계에서는 LangGraph의 기본 골격(State)을 잡고, 바로 시각 정보(OCR, Vision)를 처리하는 능력을 부여하여 흥미를 높입니다.

---

## 1주차: LangChain & LangGraph 기초 (The Skeleton)

* **학습 목표:** LLM이 생각하고 흐름을 제어하는 방식 이해
* **핵심 키워드:** `LangChain 기초`, `Graph 구조`, `State 구조`, `구조화된 출력(Structured Output)`
* **실습:**
    * 기본 Chatbot 만들기 (State 관리)
    * 사용자의 모호한 질문을 명확한 JSON 형태로 변환하는 Parser Node 만들기

---

## 2주차: 문서지능 에이전트 (The Reader - OCR)

* **학습 목표:** 비정형 문서(이미지/PDF)에서 텍스트를 추출해 랭그래프의 State로 전달하기
* **핵심 키워드:** `Azure Doc Intelligence`, `Mistral Doc AI`, `PaddleOCR`
* **실습 [OCR + LangGraph]:**
    * **PaddleOCR(로컬) vs Azure(클라우드) 성능 비교 봇:** 이미지를 업로드하면 두 엔진의 결과를 비교해 요약해주는 봇
    * **영수증 처리기:** 영수증 사진 → OCR → LLM이 항목/금액 추출 → Pydantic으로 구조화하여 State에 저장

---

## 3주차: 시각 지능 에이전트 (The Observer - Vision)

* **학습 목표:** 이미지를 이해하고 객체를 분할(Segmentation)하여 분석하기
* **핵심 키워드:** `Azure AI Vision`, `SAM3`, `Context Engineering`
* **실습 [Vision + LangGraph]:**
    * **공장 안전 관리자 봇:** 작업장 이미지 입력 → SAM으로 사람/장비 분할 → Azure Vision으로 안전장비 착용 여부 판단 → 위험 시 경고 메시지 출력
