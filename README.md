# GIT_BASIC

# Git 사용법 정리

## 0. 내가 누군지 알려주기

```sh
shift + 우클릭 -> PowerShell 창으로 열기
git config --global user.email "flowit28999@gmail.com"
git config --global user.name "flowit"
```

## 1. 초기화

```sh
git init
```

## 2. 파일 스테이징과 리포지토리 (파일의 기록을 남길 때)

```sh
git add 파일명  # 스테이징
git commit -m '메모할 내용'  # 리포지토리
```

### 2-2. 여러 파일 스테이징

```sh
git add 파일명1 파일명2 ...
git add .  # 모든 파일 스테이징
```

## 3. 상태창 열기

```sh
git status
```

## 4. commit 내역 조회하기

```sh
git log --all --oneline
```

---

## 복사본 만들기 (Branch)

### 브랜치 생성

```sh
git branch 브랜치명
```

### 브랜치로 이동

```sh
git switch 브랜치명
```

### main 브랜치로 병합

```sh
git switch main
git merge 브랜치명
```

---

## 다양한 git merge 방법

### 브랜치 삭제

```sh
git branch -d 브랜치명
```

---

## 코드 짜다가 실수 했을 경우

### 파일 복구하는 법

```sh
git restore 파일명
```

### commit 취소하는 법

```sh
git revert 커밋아이디(f6d0921)
```

### 시간을 되돌리는 법

```sh
git reset --hard 커밋아이디  # 커밋아이디 기준으로 되돌아감
```

---

## 깃허브에 코드 푸시하기

### GitHub에서 새 저장소 만들기

1. 저장소 초기화
   ```sh
   git init
   ```
2. 기본 브랜치 설정
   ```sh
   git branch -M main  # 보통 main을 사용
   ```
3. 파일 추가
   ```sh
   git add .
   ```
4. 커밋 생성
   ```sh
   git commit -m '메모 작성'
   ```
5. 원격 저장소에 코드 푸시
   ```sh
   git push -u 원격저장소주소 올릴로컬브랜치명(main)
   ```
   - 코드를 수정하고 나서도 동일한 명령어 사용

### Git에서 변수 문법 사용

```sh
git remote add 변수명(origin) 원격저장소주소  # 보통 변수명을 origin으로 사용
```

