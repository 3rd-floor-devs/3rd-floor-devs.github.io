# Node.js 설치 (Windows 전용)

사내 PC에서 사용할 기본 설치 방식과 버전 관리 방법을 정리합니다.

## 1) 직접 다운로드 설치 (nodejs.org)

단일 버전만 쓸 때 가장 단순합니다.

- [Node.js 다운로드](https://nodejs.org/){:target="_blank"}
- LTS 버전 권장
- 설치 확인:

```powershell
node --version
npm --version
```

## 2) 버전 매니저 방식 (nvm-windows)

프로젝트마다 Node 버전이 다를 때 유리합니다.

- [nvm-windows 릴리스](https://github.com/coreybutler/nvm-windows/releases){:target="_blank"}
- 설치 후:

```powershell
nvm version
nvm install 20.11.1
nvm install 18.19.1
nvm use 20.11.1
nvm list
```

## 설치 방식 차이

- 직접 다운로드: 설치가 단순하고 안정적, 단일 버전만 사용하기 좋음
- 버전 매니저(nvm): 여러 버전 전환이 쉬움, 프로젝트별 버전 고정에 유리
- npm은 패키지 관리자이며 Node 버전 관리 도구가 아님
