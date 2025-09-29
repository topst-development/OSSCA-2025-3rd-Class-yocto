#### 자기소개
안녕하세요 저는 박정윤입니다.
텔레칩스 임베디드 스쿨에 참여하여 TOPST 보드를 사용하면서 yocto를 처음 접하게 되었는데, 사용은 해보았지만 기본 지식이 아직 많이 부족한 듯 하여 신청하게 되었습니다.

----
#### git init 과  git init --bare 차이
+ git init (일반 저장소)
  + 로컬 개발용. 여기서 코드를 편집하고 커밋을 만든다.
  + 실제 파일을 수정/빌드/실행할 수 있음.
+ git init --bare
  + 주로 중앙 원격 저장소(서버용)로 사용.
  + 개발자는 이 저장소에 push/pull만 하고, 직접 파일 편집은 하지 않음.
  + 코드 파일 없이 Git 데이터만 존재.

----
#### stash
+ stash란? 아직 마무리하지 않은 작업이라 commit 하고 싶지 않지만 브랜치를 전환해야할 때 사용하는 명령어이다.
+ 이를 통해 아직 완료하지 않은 일을 commit 하지 않고 나중에 다시 꺼내와 마무리할 수 있다.
+ 기본으로는 tracked 파일 변경만 저장하지만, 새 파일까지 넣으려면 -u, 무시된 파일까지 전부면 -a를 사용하여 저장할 수 있다.
<img width="721" height="432" alt="image" src="https://github.com/user-attachments/assets/369acb31-f69a-45da-a5d4-4c15a5d23d64" />
<img width="641" height="329" alt="image" src="https://github.com/user-attachments/assets/2b596e60-c5f0-488a-bda7-0516bbcbf34d" />
<img width="660" height="78" alt="image" src="https://github.com/user-attachments/assets/e94330ce-ce1f-4a5e-a747-b5eafe9396ac" />
