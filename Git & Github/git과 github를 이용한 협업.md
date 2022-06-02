# 전반적인 Git Flow
Fork -> Clone -> Branch -> Commit & Push -> Fetch -> Solve Conflict -> Commit & Push -> Pull request

# Contributing.md
해당 Repository에 기여하기 위한 자격 요건, 어떻게 Source를 수정하고 업로드하는지에 대한 지침 등 협업을 위한 지침들을 적어놓는 문서
만약 어떤 프로젝트에 참여하게 된다면 해당 문서를 먼저 읽어보자.

# 협업 과정
## 1.Fork
Fork란 타인 소유의 Repository의 코드 내용부터, Branch, Commit 내용까지 전부 똑같이 내 소유의 Remote repository로 복사하는 작업
Fork를 통해 생성된 내 소유의 복사본을 수정하여도 원본에는 영향이 가지 않는다.
원본의 내용을 수정하고 싶다면 Pull request를 하여야 한다.

## 2.Clone
Github에 있는 Remote repository의 코드와 Commit history를 Local repository로 다운받는 작업
Local repository에서 수정한 내용을 Remote repository에 적용하기 위해서는 Commit 후 Push를 하여야 한다.

## 3.Local Repository에 원본 Repository 등록
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

## 4.Branch
기능 하나당 Branch 하나씩 만드는 편이 좋다.
수정을 여러 번 하면서 수정 이전의 소스를 잃어버리는 경우를 방지할 수 있고, 협업 과정 중 다른 사람의 수정 사항을 쉽게 적용할 수 있기 때문이다.

## 5.Commit & Push
Local repository에서 수정을 완료하였다면 Forked repository에 Commit & Push한다
물론 upstream에 바로 Commit & Push를 시도할 수도 있지만, 해당 협업 방식에서 의도하는 방법은 아니다.
upstream을 Local repository와 연결한 이유는 최신 작업 내용을 빠르게 갱신해오기 위함이다.

## 6.Fetch
Upstream repository의 Commit history를 확인한 후, 업데이트 사항이 있다면 이를 내 수정 사항에도 똑같이 적용하여야 한다.
```shell
git fetch upstream
```

## 7.Solve Conflict & Commit & Push
업데이트 사항 중 충돌하는 내용이 있다면, 이를 수정한 후 다시 Commit & Push한다
```shell
git pull
```
충돌사항 수정 후
```shell
git push origin branch1
```

## 8.Pull Request
충돌 문제를 해결한 후 원본 Repository에 병합이 가능한 상태에서 Pull request를 
