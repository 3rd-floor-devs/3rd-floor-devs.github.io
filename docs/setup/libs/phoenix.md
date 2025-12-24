# Phoenix 설치 및 기본 사용법 (Windows)

LangChain 실험 로그/트레이싱을 위한 오픈소스 도구입니다.

## 설치 (uv)

```powershell
uv venv --python 3.11
uv pip install -U arize-phoenix
```

## 서버 실행

```powershell
uv run python -m phoenix.server
```

기본 접속 주소: `http://localhost:6006`

## LangChain 연동 예시

```python
import phoenix as px
from phoenix.trace.langchain import LangChainInstrumentor

session = px.launch_app()
LangChainInstrumentor().instrument()
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
