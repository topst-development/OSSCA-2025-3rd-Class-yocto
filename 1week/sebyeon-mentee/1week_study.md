# 1주차 과제

## 목표

- 자기소개
- git 명령어 사용
- git init과 git init --bare로 만든 directory의 차이점 설명
- stash 명령어 사용 및 왜, 언제 필요할지 설명

## 1. 자기소개

1. 이름 : 변승은
2. Yocto 수업 수강 이유
   - 오픈소스 기여를 해보고 싶어서 참여하게 되었습니다.
   - Yocto는 임베디드 리눅스를 위한 빌드 시스템이라고 이해했는데, 참여하게 되면 리눅스 환경에 대한 이해에도 도움이 될 것 같았고 실제로 Yocto가 어떻게 활용되는지 (CI/CD, 보안 등)도 궁금해서 참여하고 싶었습니다.

## 2. git 명령어 사용

```
git branch 1week_seb
git checkout 1week_seb
git push -u origin 1week_seb
```

## 3. git init과 git init --bare로 만든 directory의 차이점

#### git init directory 구조

```
test-project/
 ├─ .git/         ← Git 데이터(커밋, 브랜치, 객체, 로그 등)
 │   └─ HEAD
 └─ src/          ← 실제 작업 소스 파일
```

#### git init --bare directory 구조

```
test-project.git/   ← 폴더 전체가 곧 .git/
 └─ HEAD
```

#### 차이점

- 실제 작업 소스 파일 존재 유무
- 사용 역할의 차이
  - git init : 로컬 저장소 / 분산 버전 관리 (DVCS)
  - git init --bare : 중앙 저장소 (협업의 기준점)

#### 사용이유 (추측)

- 자체 서버 / 내부망 환경에서 사용하기 위해
- 소스 배포 시 운영 반영 기준점으로 사용
- 소스 백업 용도

## 4. git stash

```
git stash
git stash list
git stash pop
```

#### 사용 이유

- checkout : commit 하지 않은 소스가 존재할 경우 checkout 불가능 하기 때문에 stash 사용 필요
- 현재 작업 소스를 다른 브랜치로 이동 시킬때 사용
- 소스 임시 저장 : commit 하기 애매한 작업 소스 임시 저장
