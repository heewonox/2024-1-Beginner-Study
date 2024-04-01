# 개발 입문 스터디 1주차

**목차**

- [Fork / Star](#fork--star)
- [Issue](#issue)
- [Branch](#branch)
- [Pull Request](#pull-request)
- [Merge](#merge)
- [실습](#실습)
- [실습 Pull Request 링크](#실습-pull-request-링크)

### Fork / Star

- Fork : 다른 사용자의 Repository를 자신의 계정으로 복사하여 독립적으로 수정하고 관리

- Star : 관심이 있는 Repository나 프로젝트에 star를 달아 "북마크"와 같이 관리

### Issue

Repository에서 작업 계획, 토론 및 추적을 위해 활용

GitHub Repository에 있는 Issue란에서 새로 생성할 수 있으며, `:memo:`와 같이 gitmoji를 사용해서 가독성을 높일 수 있다.

### Branch

기존 브랜치에서 분기되어 생성되는 별도의 작업공간으로 fork와 달리 같은 Repository에 생성됨

- `git branch` / `git branch -a`

	현재 브랜치 확인하기 / 모든 브랜치 확인하기

- `git branch "<브랜치 이름>"`

	브랜치 생성하기

- `git branch -D "<브랜치 이름>"`

	브랜치 삭제하기

- `git checkout "<브랜치 이름>"`

	브랜치 이동하기

- `git checkout -b "<브랜치 이름>"`

	브랜치 생성 후 이동하기

#### Branch Naming Convention

Commit message처럼 `"type/<issue 번호>-<간략한 설명>"`와 같이 작성하면 좋다

### Pull Request

분기된 Branch를 다시 병합하기 위한 절차로 새로운 변경을 제안하거나 병합시 발생하는 충돌을 해결하기 위하여 한다. Pull request를 보고 Merge에 앞서 코드 리뷰를 하기도 한다.

### Merge

- Merge Commit ~~(잘 모르겠으면 이걸로 머지하기)~~

	- 두 브랜치를 공통 부모로 하는 새로운 커밋을 만듦

	- A, B, C의 커밋이 그대로 main 브랜치로 병함


- Squash and Merge

	- A, B, C의 커밋을 하나의 커밋으로 main 브랜치로 병합

- Rebase and Merge
	
	- A, B, C 커밋의 base를 재설정, 모두 새로운 커밋으로 변경

	- commit hash가 변경되며 사용에 주의

### 실습

브랜치 생성 -> 브랜치에서 add, commit -> 브랜치에서 push -> GitHub Pull Request 에서 Merge

### 실습 Pull Request 링크

[https://github.com/heewonox/2024-1-Beginner-Study/pull/2](https://github.com/heewonox/2024-1-Beginner-Study/pull/2)