# 전반적인 Git Flow
Fork -> Clone -> Branch -> Commit & Push -> Fetch -> Solve Conflict -> Commit & Push -> Pull request

# Contributing.md
해당 Repository에 기여하기 위한 자격 요건, 어떻게 Source를 수정하고 업로드하는지에 대한 지침 등 협업을 위한 지침들을 적어놓는 문서
만약 어떤 프로젝트에 참여하게 된다면 해당 문서를 먼저 읽어보자

# Fork
Fork란 타인 소유의 Repository의 코드 내용부터, Branch, Commit 내용까지 전부 똑같이 내 소유의 Remote repository로 복사하는 작업
Fork를 통해 생성된 내 소유의 복사본을 수정하여도 원본에는 영향이 가지 않는다.
원본의 내용을 수정하고 싶다면 Pull request를 하여야 한다.

# Clone
Github에 있는 Remote repository의 코드와 Commit history를 Local repository로 다운받는 작업
Local repository에서 수정한 내용을 Remote repository에 적용하기 위해서는 Commit 후 Push를 하여야 한다.

# Local Repository에 원본 Repository 등록
Clone 직후 Local repository가 바라보고 있는 Remote repository는 Forked repository이다.
이는 다음 명령어로 확인할 수 있다.
```shell
git remote -v
```
Forked repository는 origin이라는 명칭으로 등록되어 있다.

이 때, 원본 Repository를 Local repository와 연결시켜 줌으로써, 원본 소스가 수정되었을 때 바로 수정 사항을 Local repository에 적용시킬 수 있다.
적용하는 법은 다음과 같다
```shell
git remote add <upstream> <원본 Repository의 주소>
```
> upstream은 통상적으로 사용하는 명칭이므로, 다른 이름으로 등록하여도 상관없다.

