# 개발 입문 스터디 1주차

**목차**

- [git 이란](#git-이란)
- [파일의 생명주기](#파일의-생명주기)
- [git의 영역](#git의-영역)
- [git으로 파일 관리하기](#git으로-파일-관리하기)
- [git에서 GitHub로 (GitHub에서 로컬 저장소로)](#git에서-github로-github에서-로컬-저장소로)
- [GitHub에서는 이런 것도 가능합니다](#github에서는-이런-것도-가능합니다)
- [GitHub에 올리기](#github에-올리기)
- [Commit Message Convention](#commit-message-convention)
- [실습 Repository 링크](#실습-repository-링크)


### git 이란

git은 버전 관리 및 협업을 위해 사용하는 오픈소스 소프트웨어이며

- 어떤 파일이 수정 되었는지
- 누가 수정 했는지
- 언제 수정되었는지
- 어떻게 수정되었는지
	
를 추적하고 원하는 상태의 코드를 사용하기 위해서 사용한다.
	
### 파일의 생명주기

- Untracked

	파일이 git에의해 추적되지 않는 상태

- Unmodified

	최근 커밋 이후 변경사항이 없는 상태

- Modified

	파일에 변경 사항이 있으나 아직 Staging Area로 추가되지 않은 상태
	
	`git status` 명령어를 통해 수정된 파일을 확인할 수 있음

- Staged

	수정된 파일이 Staging Area에 추가된 상태


### git의 영역

- Working Directory

	사용자가 현재 작업하고 있는 디렉토리

- Staging Area

	변경된 파일들이 일시적으로 대기하는 곳

- Repository (Local Repo, Remote Repo)

	프로젝트의 모든 변경 이력이 저장되는 곳

### git으로 파일 관리하기
	
- `git init`
		
	디렉토리에 git 저장소를 만들기

- `git add`

	git으로 관리할 대상 등록 (파일이 staged 됨)

- `git commit`

	파일 수정 후 로컬 저장소(Local Repo)로 옮기기

파일을 unstage로 되돌리고 싶다면 `git rm --cached <파일명>`

git으로 관리를 그만하고 싶다면 `rm -r .git`

### git에서 GitHub로 (GitHub에서 로컬 저장소로)

- `git push`

	로컬 저장소의 커밋들을 원격 저장소로 전송

- `git pull`

	원격 저장소의 최신 변경 사항을 가져와 로컬 저장소에 병헙함

- `git clone`

	원각 저장소의 내용을 복제하여 로컬 컴퓨터로 가져옴

	원격 저장소의 모든 내용이 로컬로 복제되어 새로운 로컬 저장소가 생성됨

### GitHub에서는 이런 것도 가능합니다
	
- 이슈 트래킹
- 코드 리뷰
- GitHub Actions를 통한 CI(Continuous Integration)/CD(Continuous Deployment)
- GitHub Projects를 통한 프로젝트 업무 관리

### GitHub에 올리기

- 올리기에 앞서

	```sh
	git remote add origin <주소>
	git branch -M main
	git push -u origin main
	```

- GitHub에 올리기

	```sh
	git add <파일명>
	git commit -m "커밋 메세지"
	git push origin main
	```


### Commit Message Convention

`type : subject` 형식으로 작성하면 좋다
	
- feat : 새로운 기능을 추가한 경우

- refactor : 기존 코드를 개선한 경우

- fix : 버그를 수정한 경우

- chroe : 코드 외의 설정을 바꾼 경우

- docs : 문서화

- test : 테스트 코드

### 실습 Repository 링크

[https://github.com/heewonox/heewonox](https://github.com/heewonox/heewonox)