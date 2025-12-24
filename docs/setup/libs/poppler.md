# Poppler 설치 및 환경변수 설정 (Windows)

PDF 처리 도구(예: pdf2image 등)에서 Poppler 바이너리가 필요할 때 사용합니다.

## 1) C 드라이브에 설치하고 전역 PATH 설정

1. Poppler for Windows 배포본을 다운로드합니다.
2. 압축을 풀어 `C:\poppler`에 위치시킵니다.
3. `C:\poppler\Library\bin`을 PATH에 추가합니다.

### PATH 설정 방법

- 시작 메뉴에서 “환경 변수” 검색 → “시스템 환경 변수 편집”
- “환경 변수” → “Path” → “새로 만들기”
- `C:\poppler\Library\bin` 추가 후 확인
- 새 터미널을 열어 적용 확인

확인:

```powershell
where pdfinfo
pdfinfo -v
```

## 2) 프로젝트 내부에 설치하고 경로 지정

프로젝트 폴더에 Poppler를 넣고, 실행 시 경로를 명시합니다.

예시 구조:

```
project-root/
  tools/
    poppler/
      Library/
        bin/
```

### 환경변수로 지정 (권장)

PowerShell에서 현재 세션만 적용:

```powershell
$env:POPPLER_PATH = "C:\path\to\project-root\tools\poppler\Library\bin"
```

코드에서 `POPPLER_PATH`를 읽어 사용합니다.

### 직접 경로 지정 예시 (Python)

```python
from pdf2image import convert_from_path

images = convert_from_path(
    "sample.pdf",
    poppler_path=r"C:\path\to\project-root\tools\poppler\Library\bin",
)
```

## 참고 링크

- [Poppler for Windows](https://github.com/oschwartz10612/poppler-windows){:target="_blank"}
