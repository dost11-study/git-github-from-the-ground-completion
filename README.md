# git-github-from-the-ground-completion
인프런의 [Git & GitHub, 원리부터 차근차근 - 근본깃 [완성편]](https://www.inflearn.com/course/geek-%EA%B7%BC%EB%B3%B8%EA%B9%83-git-github)를 정리한 내용입니다.

## cherry-pick

다른 브랜치의 특정 커밋 하나를 현재 브랜치에 가지고 오고 싶다면
`git cherry-pick [커밋 ID]`를 사용하면 된다

`cherry-pick`도 `merge`처럼 `diff`를 통해 가져오기 때문에 conflict가 날 수 있다
conflict가 날 경우 staging area에서 unmerged path 상태가 되면서 commit 생성 과정에 실패한다 (수동 conflict 해결 필요)
staging area의 conflict를 해결하고 다시 add 한 후 `git cherry-pick --continue`를 통해 체리픽 커밋을 생성한다

## 브랜치를 이동할 때 주의할 점

- 다른 브랜치로 이동할 때, working directory나 staging area에 수정한 내용이 남아 있으면 안됨
- 다른 브랜치로 이동할 수 없다고 오류가 뜸
- 수정할 내용을 Commit으로 저장하면, 다른 브랜치로 이동할 수 있음 (stash도 가능)

**working directory clean**
- untracked 상태는 비어있고, tracked 상태와 staging area 그리고 최신 커밋이 똑같은 상태일 경우
- working directory clean 상태에서는 다른 브랜치로 이동이 가능하다

## 


