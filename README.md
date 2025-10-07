# git-github-from-the-ground-completion
인프런의 [Git & GitHub, 원리부터 차근차근 - 근본깃 [완성편]](https://www.inflearn.com/course/geek-%EA%B7%BC%EB%B3%B8%EA%B9%83-git-github)를 정리한 내용입니다.

## cherry-pick

다른 브랜치의 특정 커밋 하나를 현재 브랜치에 가지고 오고 싶다면
`git cherry-pick [커밋 ID]`를 사용하면 된다

`cherry-pick`도 `merge`처럼 `diff`를 통해 가져오기 때문에 conflict가 날 수 있다
conflict가 날 경우 staging area에서 unmerged path 상태가 되면서 commit 생성 과정에 실패한다 (수동 conflict 해결 필요)
staging area의 conflict를 해결하고 다시 add 한 후 `git cherry-pick --continue`를 통해 체리픽 커밋을 생성한다

