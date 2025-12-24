# Playwright 설치 및 기본 사용법 (Windows)

Python 환경은 uv로 통일합니다. 아래는 Windows 기준입니다.

## Python 설치 (uv)

```powershell
uv venv --python 3.11
uv pip install playwright
uv run playwright install
```

## 기본 사용법

### 코드 생성 (codegen)

```powershell
uv run playwright codegen https://example.com
```

### 간단한 스크립트 실행 (Python)

```powershell
uv run python script.py
```

## 참고 링크

- [Playwright 공식 문서](https://playwright.dev/){:target="_blank"}
