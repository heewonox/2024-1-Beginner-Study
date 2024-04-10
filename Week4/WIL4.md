# 개발 입문 스터디 4주차

**목차**

- [브랜치 전략](#브랜치-전략)
- [Branch Strategy : Git Flow](#branch-strategy--git-flow)
- [Branch Strategy : GitHub Flow](#branch-strategy--github-flow)
- [Attitude as a Dev](#attitude-as-a-dev)

### 브랜치 전략

> 이해가 안되시죠... 실제 적용해보면서 엉엉 울어도 보면서 강해지셔야 합니다...

#### 브랜치 관리의 필요성

1. 서로의 작업에 영향을 주지 않기 위해 브랜치의 분리가 필요하다

2. 각 브랜치가 어떤 작업을 위해 존재하는지 구분이 필요하다

3. main 브랜치의 안전한 관리가 필요하다

#### 브랜치 보호 규칙

승인 없이 Pull Request를 병합할 수 없도록 제한하고 특정 브랜치에 Push 가능자를 제한하여 브랜치를 안전하게 관리할 수 있다.

### Branch Strategy : Git Flow

<img src="https://raw.githubusercontent.com/heewonox/test1/main/git_flow__.png" style="width: 60%">

#### 브랜치 종류

- Main Branches (영원히 존재하는 브랜치)
	
	- main (master)

		프로젝트 생성 시 기본으로 생성되는 브랜치이며 병합될 때마다 제품의 새로운 버전이 탄생한다.
		
		배포되어 있는 환경이라고 생각하시면 편하다....

	- develop

		feature 브랜치의 기반으로 새로운 기능과 변화가 병합되는 브랜치이다

- Supporting branches
	
	- feature
		
		특정한 기능을 개발하는 브랜치로 develop 브랜치에서 분기하여 작업한다.

		기능 개발 완료 후 develop 브랜치로 머지 한 다음 유지 하지 않고 삭제해도 된다...

		main, master, develp, release, hotfix 등의 특정한 용어를 제외하고 대부분의 이름을 써도 된다

	- release

		배포 준비를 위한 브랜치로 develop 브랜치에서 버그가 존재할 수 있기 때문에 여기서 자잘한 버그를 수정하고 QA(Quality Assurance) 작업을 한다

		devlop 브랜치에서 분기하여 main + develop 브랜치로 병합한다...

	- hotfix

		배포 환경에서 즉각적인 수정이 필요한 경우 사용하며 main 브랜치에서 분기하여 main, develop 모두에게 병합한다

### Branch Strategy : GitHub Flow

<img src="https://raw.githubusercontent.com/heewonox/test1/main/git_flow__.png" style="width: 60%">

Git Flow가 배포가 수시로 이루어지는 현 시대의 웹앱에는 부적합하여서 고안한 방법이다

GitFlow를 개발한 Vincent Driessen도 이와 같은 전략을 추천한다

- main

	항상 배포 가능 상태로 유지하며 develop과 release가 사라졌기 때문에 main으로 병합하기 전에는 충분한 테스트가 필요하다

- feature

	main에서 분기하여 작업 후 다시 main으로 병합한다
	
	Git Flow와는 달리 이외 브랜치들을 구분하지 않으므로 브랜치의 목정을 이름에 잘 담아야 하며, Git Flow에 비해 코드 리뷰의 중요성이 더 크다

### 그래서 어떤 전략을 사용해야 하는가

상황에 맞게... 항상 그대로 따를 필요도 없다...

### Attitude as a Dev

#### Convention을 만들어 사용하자

긴 시간이 지난 후에 봐도 쉽게 의도를 파악할 수 있으며 <span style="color: rgb(105,277,208); font-weight:bold">보기 좋은 프로젝트</span>가 된다

#### 코드에 대한 주인 의식

Public Repository에 있는 코드는 남들도 다 볼 수 있다

사람을 구할때 코드도 보고 팀 프로젝트에서 지켜야 할 것들을 잘 지키면서 개발하는지 다 보기 때문에

돌아가기만 하는 코드보다는 잘 설계된 코드를 짜보도록 노력하자

#### 질문을 <span style="color: rgb(105,277,208)">잘</span> 하자

구글과 ChatGPT가 해결해주지 못하는 문제들이 존재한다

내가 어떤부분에서 막혔고 해결하기 위해서 어떤걸 시도해보았는지 명확히 밝히면서 

좋은 질문을 할 수 있도록 노력하자


