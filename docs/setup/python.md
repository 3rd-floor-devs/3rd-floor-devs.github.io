# Python 설치 (Windows 전용)

사내 PC에서 사용하는 기본 설치 방법과 버전 관리 방식을 정리합니다.

## 1) 직접 다운로드 설치 (python.org)

단일 버전만 사용할 때 가장 간단합니다.

- [Windows용 Python 다운로드](https://www.python.org/downloads/windows/){:target="_blank"}
- 설치 시 `Add python.exe to PATH` 체크
- 설치 확인:

```powershell
python --version
pip --version
```

## 2) Python install manager (pymanager)

Windows용 공식 설치/관리 도구입니다. 기존 Python launcher와 `py` 명령이 겹치므로, 이전 launcher는 제거하는 것을 권장합니다.

### 설치 방법

- Microsoft Store: [Python install manager](https://apps.microsoft.com/detail/9NQ7512CXL7T){:target="_blank"}
- WinGet:

```powershell
winget install 9NQ7512CXL7T
```

- MSIX 다운로드: [Python install manager 25.2](https://www.python.org/downloads/release/pymanager-252/){:target="_blank"}

### 기본 사용

```powershell
# 사용 가능한 패키지 목록
py list --online

# 초기 구성 점검
py install --configure
```

### 여러 버전 설치 (예시)

```powershell
py install 3.12
py install 3.11
```

### 기본 버전 설정 (환경 변수)

```powershell
setx PY_PYTHON 3.11
```

환경 변수 변경 후에는 새 터미널을 열어 확인합니다.
