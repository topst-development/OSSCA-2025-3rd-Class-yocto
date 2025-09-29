## 자기 소개
Yocto가 궁금하기도 했고, TOPST D3-G 우분투 이미지를 직접 빌드해보고 싶었습니다.
레트로 게임 OS 빌드도 Yocto로 해보고 싶었으나 찾아보니 Yocto를 지원하지 않아 할수 없게 되었네요.

## git init, git init --bare 차이
### git init
일반적으로 흔히 쓰는 형태입니다.
로컬에 git working directory를 만듭니다.
또한 .git 디렉터리가 만들어지고 git 메타데이터가 생깁니다.
git add, git commit 등을 할 수 있습니다.
### git init --bare
한번도 써본적이 없네요.
working directory가 없고 git 메타데이터만 있습니다.
파일 수정/빌드 목적이 아니라 오직 push/pull을 위한 원격 저장소입니다.
일반적으로 서버에 만들어 두고 개발자들이 git clone, git push, git pull 할때 씁니다.
## git stash
아직 커밋하지 않았고 한창 작업중인데, 다른 브랜치로 체크아웃 해야 할때
잠깐 저장해 놓고 나중에 다시 원복 시킬수 있음

