노영재

4학년 대학생이고 현재 개발자로 취업 준비 중인 취준생입니다!

##  왜 Yocto 수업을 듣나
- 배포판이 아닌 **메타데이터로 이미지 정의**하는 방식이 궁금해서
- 레시피/레이어를 통해 **패키징-이미지 생성-크로스 컴파일**까지 한 번에 배우려 함

- 실제 프로젝트에 **재현 가능한 빌드 + CI**를 적용하고 싶어서


## 1) `git init` vs `git init --bare`
- `git init`
  - 현재 폴더를 **작업 가능한 로컬 저장소**로 초기화
  - 워킹 디렉토리(실제 파일) + `.git/` 메타데이터가 함께 존재
  - 개발자가 **파일 수정/커밋**하는 데 사용

- `git init --bare`
  - **워크트리(작업 폴더) 없음**. `.git` 내용만 있는 **순수 저장소**
  - 주로 **원격 저장소(협업용 중앙 저장소)** 로 사용 (편집 X, push/pull O)
  - 예) 사내 NAS 경로에 `project.git` 생성 후 팀이 origin으로 사용

## 2) `git stash` 실습: 왜/언제/어떻게
- **왜/언제?**
  - 작업 중 변경사항이 있는데(미완성) **다른 브랜치로 급히 이동**해야 할 때
  - 아직 커밋하고 싶지 않을 때 **임시로 변경사항을 숨김(보관)**

- **사용 예시**
  ```bash
  # 변경사항 임시 보관 (추적되지 않은 파일도 포함하려면 -u)
  git stash push -u -m "WIP: yocto intro page"

  # 보관 목록 확인
  git stash list

  # 가장 최신 stash 적용만 (목록 유지)
  git stash apply

  # 적용 + 목록에서 제거(팝)
  git stash pop

  # 특정 항목만 적용 (예: stash@{2})
  git stash apply stash@{2}

  # stash에서 바로 새 브랜치 만들어 이어서 작업
  git stash branch feature/from-stash stash@{0}