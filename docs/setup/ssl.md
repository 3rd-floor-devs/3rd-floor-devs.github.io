# SSL/인증서 문제 해결 (Windows)

LLM 요청 등에서 `SSL` 오류가 발생하는 경우, 사내 PC의 OS 신뢰 저장소를 사용하도록 설정하면 해결되는 경우가 많습니다.

## 해결 방법 요약

- **truststore**: SSL 레벨에서 OS 신뢰 저장소를 주입 (범용성 높음)
- **pip-system-certs**: requests/urllib3 계열에서 OS 신뢰 저장소 사용 (간단 적용)

## truststore 방식 (권장)

설치:

```powershell
uv add truststore
```

코드에 추가:

```python
import truststore
truststore.inject_into_ssl()
```

## pip-system-certs 방식

설치:

```powershell
uv add pip-system-certs
```

환경 변수:

```
PIP_USE_CERTIFI=0
```

## 어떤 게 유리한가

- 범용성/유지보수 관점에서는 **truststore**가 더 유리합니다.
- requests 위주라면 **pip-system-certs**도 충분하지만, 다른 스택에는 제한적일 수 있습니다.

## 표준화 추세 의미

truststore는 Python 생태계에서 OS 신뢰 저장소를 일관되게 쓰기 위한 공통 접근으로 자리 잡는 흐름이 있습니다.  
라이브러리마다 제각각이던 “certifi vs OS 저장소” 문제를 SSL 레벨에서 통일하려는 방향입니다.
