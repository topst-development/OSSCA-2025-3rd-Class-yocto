## 1주차

##### 1. git init과 git init --bare로 만든 directory의 차이
##### 2. stash 명령어의 사용 
----
### 1. git init과 git init --bare로 만든 directory의 차이
* bare 저장소: 워킹 디렉토리가 없는 저장소
```
$ cd /srv/git
$ mkdir project.git
$ cd project.git
$ git init --bare
Initialized empty Git repository in /srv/git/project.git/
```
my-project.git 디렉터리 안에 bare repository가 생성되고, 이 디렉터리는 이제 다른 개발자들이 코드를 푸시할 수 있는 원격 저장소 역할을 하게 됩니다.

### 2. stash 명령어의 사용 
당신이 어떤 프로젝트에서 한 부분을 담당하고 있다고 하자. 그리고 여기에서 뭔가 작업하던 일이 있고 다른 요청이 들어와서 잠시 브랜치를 변경해야 할 일이 생겼다고 치자. 그런데 이런 상황에서 아직 완료하지 않은 일을 커밋하는 것이 껄끄럽다는 것이 문제다. 커밋하지 않고 나중에 다시 돌아와서 작업을 다시 하고 싶을 것이다. 이 문제는 git stash 라는 명령으로 해결할 수 있다.

<mark>Stash 명령을 사용하면 워킹 디렉토리에서 수정한 파일들만 저장한다. Stash는 Modified이면서 Tracked 상태인 파일과 Staging Area에 있는 파일들을 보관해두는 장소다.</mark> 아직 끝내지 않은 수정사항을 스택에 잠시 저장했다가 나중에 다시 적용할 수 있다(브랜치가 달라져도 말이다).

```bash
$ git stash (or git stash save)  # 스택에 새로운 Stash 생성 
$ git stash list # 저장한 Stash 확인 
$ git stash apply stash@{2}  # Stash 적용, 이름 없으면 가장 최근의 Stash 적용
$ git stash drop # 스택에서 Stash 제거
$ git stash pop # Stash 적용 후 스택에서 바로 제거
```


참고: https://git-scm.com/book/ko/v2/Git-%eb%8f%84%ea%b5%ac-Stashing%ea%b3%bc-Cleaning

