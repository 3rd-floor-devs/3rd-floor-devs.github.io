# UV 설치 및 초기화

uv는 Python 패키지 관리와 가상환경을 빠르게 다루는 도구입니다.

## 설치

### Windows

```powershell
irm https://astral.sh/uv/install.ps1 | iex
```

설치 확인:

```bash
uv --version
```

## 프로젝트 초기 설정

다음 흐름을 기본으로 합니다.

1. 저장소 생성
2. uv로 가상환경 및 의존성 설정
3. 실행 방법 문서화

### 예시

```bash
# 1) 새 폴더
mkdir my-study-project
cd my-study-project

# 2) uv로 가상환경 만들기 (버전 지정 가능)
uv venv --python 3.11

# 3) 의존성 추가
uv add fastapi

# 4) 실행
uv run python -m pip list
```

## venv에서 Python 버전 지정

```bash
uv venv --python 3.11
uv venv --python 3.12
```

## 일반적인 실행 방법

```bash
# 가상환경 실행
uv run python app.py

# 패키지 모듈 실행
uv run pytest
```

## uv pip install vs uv add 차이

- `uv pip install`: pip 호환 방식으로 즉시 설치만 수행 (프로젝트 메타데이터 업데이트 없음)
- `uv add`: 프로젝트 의존성으로 기록하고 설치까지 수행 (권장)

예시:

```bash
uv pip install requests
uv add requests
```

## uv init

새 Python 프로젝트 기본 구조를 빠르게 생성합니다.

```bash
uv init
```
