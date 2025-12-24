# Phoenix 설치 및 기본 사용법 (Windows)

LangChain 실험 로그/트레이싱을 위한 오픈소스 도구입니다.

## 서버 설치 (별도 터미널에서 실행)

```powershell
uv venv --python 3.11
uv pip install -U arize-phoenix
```

## 서버 실행

```powershell
uv run phoenix serve
```

기본 접속 주소: `http://localhost:6006`

## 프로젝트 설치 (추적/연동용)

```powershell
uv add arize-phoenix-otel openinference-instrumentation-langchain
```

## LangChain 연동 예시 (레지스터)

```python
from phoenix.otel import register

tracer_provider = register(
    project_name="tracing-test1",
    auto_instrument=True
)
```

```python
from langchain_openai import ChatOpenAI
from langchain_core.messages import HumanMessage

llm = ChatOpenAI(model="gpt-4o-mini")
response = llm.invoke([HumanMessage(content="Hello Phoenix")])
print(response.content)
```

## 참고 링크

- [Phoenix GitHub](https://github.com/Arize-ai/phoenix){:target="_blank"}
