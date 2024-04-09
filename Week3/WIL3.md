# 개발 입문 스터디 3주차

**목록**

- [`git log`](#git-log)
- [`git status`](#git-status)
- [amend](#commit---amend)
- [reset](#reset)
- [revert](#revert)

### `git log`

commit 기록을 최신순으로 확인 할 수 있다

HEAD는 현재 작업 중인 위치를 가리키며 현재 작업중인 브랜치의 가정 최근 commit이면서 다음 commit의 base가 되는 commit이다. 새로운 commit이 생기면 HEAD도 변경된다.

### `git status`

Untracked, Modified, Staged의 세 가지 상태에 따라 파일을 분류하여 확인할 수 있다.

### commit --amend

마지막 commit의 내용에 변경이 있을 때 사용하며 완전히 새로운 commit으로 대체하기 때문에 commit id가 바뀐다.

다른 사람이 작업 기반으로 삼고 있는 commit은 amend하지 말아야 한다

`git commit --amend -m "commit message"` : vim 진입 없이 commit 메시지 수정

`git commit --amend --no-edit` : commit 메시지 수정 없이 commit 수정

### reset

commit을 제거하는데 사용한다

- soft

	커밋만 취소하며 변경 사항이 Staging Area로 돌아간다

- mixed (기본)
	
	커밋을 취소하며 변경 사항이 Working Directory로 돌아간다

- hard

	커밋을 취소하며 변경 사항을 모두 제거하고 이전 커밋으로 돌아간다

### revert

commit을 제거하지 않고 되돌리며 되돌리기 위해서 새로운 commit이 생성된다.

`--no-commit` 옵션을 사용해서 직접 commit하지 않고, revert한 내용을 Staging Area에 올리도록 할 수 있다.

reset은 commit을 삭제하므로 commit을 공유하는 다른 브랜치에도 영향을 줄 수가 있다. 그러므로 commit을 삭제하기보다 생성하여 되돌리는 revert가 안전하다.