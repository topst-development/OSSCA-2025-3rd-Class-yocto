### 자기소개
안녕하세요!
오픈소스 생태계 그리고 Yocto에 관심이 생겨 이번에 함께 참여하게 되었습니다:)

1. git init과 git init --bare로 만든 directory의 차이점을 설명
   - git init : git repository를 생성함과 동시에 작업 공간을 함께 생성
     이때 만든 레포지토리를 non-bare git repository라고도 함
   - git init --bare : git repository만 생성
     bare git repository라고도 함
     작업 영역이 없기 때문에 안에서 파일을 추가, 수정, 삭제 등을 할 수 없음
2. git stash란
   변경사항을 일시적으로 저장하는 기능으로, 아직 커밋하기엔 이른 경우나 다른 브랜치로 체크아웃할 때 변경사항을 유지하고 싶을 때 사용할 수 있음
   - 사용하는 이유
     1. 변경사항을 커밋하기엔 아직 이른 경우
     2. 다른 브랜치로 체크아웃할 때 변경사항을 유지하고 싶은 경우
     3. 변경사항을 일시적으로 저장하고 싶은 경우
   - 사용할 수 있는 명령어
     1. git stash : 현재 작업 중인 변경 사항을 일시적으로 저장하고, 작업 디렉토리를 깨끗한 상태로 만듬
     2. git stash pop : 스택에 쌓인 가장 최근의 변경 사항을 불러와 작업 디렉토리에 적용
     3. git stash apply : 스태시를 적용한 후에도 스태시가 적용되어 있는 상태를 유지
     4. git stash list : 현재 stash들의 목록을 확인 가능
