   . git 명령어를 사용해 본 내
     .. 꼭 git init과 git init --bare로 만든 directory의 차이점을 설명으로 올려 주세요.
     .. 꼭 stash 명령어를 사용해 보고 왜, 언제 필요할지 설명으로 올려 주세요.


     1. git init과 git init --bare로 만든 directory의 차이점을 설명
     .. git init : creates git repository + workspace
     ....작업 영역을 통해 파일을 추가, 수정, 삭제 가능
     .. git init --bare : creates only git repository
     ....작업 영역이 없기에 파일을 추가, 수정, 삭제 불가
    출처 : https://jjam89.tistory.com/163


    2. git stash
    ..git stash 사용 이유 : 변경 작업을 임시로 저장하기 위해서
    ..git stash 명령어 사용

    ..[git stash하면 내가 add 한 파일이 안 보이는 이유]
    ..git add 파일명 해서 새로 만든 파일을 스테이징 후 아직 commit이 없음
    ..git stash(기본) 는 워킹트리와 스테이징 상태 둘 다를 저장해두고, 작업 디렉토리를 마지막 커밋(HEAD) 상태로 되돌려 놓음.
    ..그런데 my_intro.md는 **HEAD에는 없는 “새 파일”**이었지.
    ..→ 그래서 stash 후에 워킹트리에서 파일이 없어 보이는 것 / “삭제”된 게 아니라 stash 안으로 들어간 것!

    ..[안 보이는 파일 되살리기]
    ..1. 어떤 stash에 들어갔는지 보기
    ..git stash list
    ..git stash show -p stash@{0} # 내용 미리보기(패치)
    ..2. 전체를 복구하고 해당 stash를 지우기
    ..git stash pop # 충돌 나면 해결 후 add/commit
    ..(지우지 않고 적용만 하려면 git stash apply)
    ..3. 파일만 꺼내고 싶다면
    ..특정 파일만 복원 (현재 디렉토리로)
    ..git checkout stash@{0} -- my_intro.md
    ..또는 git restore --source=stash@{0} -- my_intro.md
