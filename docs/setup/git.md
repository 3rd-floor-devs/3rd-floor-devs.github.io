# Git 설치와 기본 명령어

사내 저장소 사용을 위한 Git 설치와 기본 작업 흐름을 정리합니다.

## 설치

### Windows

- [Git for Windows 다운로드](https://git-scm.com/download/win){:target="_blank"}
- 설치 후 `git --version`으로 확인

## 기본 설정

```bash
git config --global user.name "홍길동"
git config --global user.email "hong@example.com"
```

## 저장소 시작

```bash
# 새 저장소 시작
git init

# 원격 연결
git remote add origin <repo-url>
```

## 클론

```bash
git clone <repo-url>
```

## 기본 흐름

```bash
git status
git add .
git commit -m "메시지"
git push
```

## 되돌리기

### 최근 커밋 되돌리기 (이력 유지)

```bash
git revert HEAD
```

### 작업 내용 되돌리기

```bash
# 파일 단위
git restore <file>

# 스테이징 취소
git restore --staged <file>
```

## 강제 푸시

```bash
git push --force-with-lease
```

주의: 팀과 공유하는 브랜치에서는 사용을 피하고, 필요한 경우 팀에 먼저 공유합니다.
