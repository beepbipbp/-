# 1. git config --global

```bash
git config --global user.name "username1" // username 세팅
git config --global user.email "aaa1@bbb1.com" // email 세팅
git config --list // 세팅 확인
```

# 2. init, add, commit, status, log, reset

```bash
git init // .git 디렉토리 생성(사진사 고용)
git add . // 해당 폴더 내의 파일들의 스테이징 시작(사진찍을 사람들 모으기)
git commit -m "name1" // 스테이징 된 파일들을 name1이라는 이름으로 저장(사진 찍기)
git status // 현재 git 상태를 보여줌
git log // commit log를 확인
git reset --hard commithashcode1 // commithashcode1의 commit으로 코드를 롤백
```

# 3. github remote 연동

```bash
git remote add origin repositoryaddress1 // repository와 local 폴더를 연결
git push origin main(branch) // github repository main(branch)에 현재 커밋들을 넣는다
git clone repositoryaddress1 // github repository에서 모든 커밋들을 내 local 폴더로 가져온다
git pull origin main(branch) // 서버에서 변경사항이 일어난 것을 local로 동기화한다
git remote rm origin // remote origin 
```
