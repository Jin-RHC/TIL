# git 명령어 모음 

> git 기본 명령어 정리

### git 생성


- 현재 폴더를 git으로 관리하겠다!
- 현재 폴더에 `.git` 폴더를 생성
- 최초 한 번만 실행하는 명령어

```bash
git init
```



### 확인

- version 체크

```bash
git --version
```


- branch master인지 알려면. 현재 git이 관리하고 있는 파일들의 상태를 보여주는 명령어

```bash
git status
```

- config 과정

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
//완료 확인:
git config --global user.name
git config --global user.email
```



### 관리(로컬): add, commit

> working directory에서 작업(수정)한 파일을 index(staging area)에 업로드(add)하고 그렇게 쌓인 커밋할 목록을 commit하고 쌓인 커밋들을인 head를 GitH햐ub에 push하는 일련의 과정



- add: 커밋에 단일 파일의 변경 사항을 포함. working directory에서 staging area에 파일을 업로드.
  - `.`: 현재 폴더, 하위 폴더, 하위 파일 모두(리눅스에서 .은 폴더를 의미)

```bash
git add <file name>
git add .
```

- commit: staging area에 올라온 파일들을 하나의 커밋으로 만들어주는(스냅샷 찍는) 명령어

```bash
git commit -m "커밋 메세지" // 리눅스에서 -가 붙으면 옵션을 뜻함.
git commit -m "add README.md" // README.md를 올리려면
git log // 커밋의 히스토리를 보여주는 명령어
```

- 원격 서버 등록 후 push하는 과정(master branch를)



### 관리(원격): push 등

- 원격 저장소 주소를 로컬에 저장하는 명령어
  - nickname에는 일반적으로 `origin`

```bash
git remote add <nickname> <url>
git remote add origin https://github.com/Jin-RHC/TIL.git //example
```



- push

```bash
git push <nickname> <branch name>
git push origin master


git push remote add origin https://github.com/Jin-RHC/TIL.git
```



