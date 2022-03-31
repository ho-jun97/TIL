# git flow 명령어
- 초기화 : git flow init

- 새 기능 시작하기 : git flow featrue start 이름

- 기능완료 : git flow featrue finish 이름

- 기능을 게시 : git flow feature publish 이름
	- 다른 개발자들의 릴리스 commit을 허용하기 위한 행위

- release 시작 : git flow release start v(버전)
	- v0.0.0 v(제일큰업데이트 등.중간업데이트 등.작은버그 수정 등)

- release 종료 : git flow release finish v(버전)

- tag push : git push --tags
	- v0.0.1과 같은 버전 등등


# git flow 구조
- main
- develop
	-feather/(NAME)

- (hotfix)-master-(release)-develop-feature
	- master : 제품으로 출시될 수 있는 브랜치(보통 main)
	- hotfix : 출시 버전에 문제가 생기면 해결하기 위한 브랜치
	- release : 이번 출시 번전을 준비하는 브랜치
	- develop : 다음 출시 버전을 개발하는 브랜치
	- featrue : 기능을 개발하는 브랜치



