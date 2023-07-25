# ABOUT BRANCH

## Branch는 무엇인가?

![beanch](./assets/branch.png)
- 독립적으로 작업을 진행하기 위한 개념
- `master branch`란 모든 `repository`의 기본 혹은 메인
- `master branch`로부터 파생된 다른 `branch`들로부터 수정 사항을 만든 다음 `master`에 병합하는 과정을 거침

## Branch 생성
1. `git branch <branch name>`로 Branch 생성
2. `git branch`로 현재 위치한 Branch 확인
3. `git switch <branch name>`으로 원하는 Branch로 이동
4. `git push origin <branch name>`으로 Repository에 branch 생성 
5. `Pull requests`로 branch 내용 master로 합병 가능

- `merge`가 된 branch는  delete하는 것이 일반적