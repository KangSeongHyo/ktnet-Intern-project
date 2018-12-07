# SVN

설명
----

Git처럼 형상관리를 위한 협업 Tool

환경 구성 (window)
------------------

1.	Visual SVN (Server)
2.	Tortoise SVN (Client)

Visual SVN
----------

SVN 서버를 만들때 사용(443 port)

#### Repository 생성하기

> 1.	Visual SVN 실행
> 2.	Repositories 클릭하여 create new Repository 클릭
> 3.	Custom 클릭 후 add를 사용하여 사용자등록(권한 부여) Propertise에서도 가능
> 4.	모든작업 -> Browse 클릭하면 Repository 내용을 볼 수 있음

#### Repository에 Commit하기

> 1.	원하는 폴더 선택 후 왼쪽 클릭 Tortoise SVN -> import
> 2.	message부분에 commit message 작성
> 3.	Ok 하면 Browse에서 볼 수 있음

#### SVN 형상관리

팀원 한명이 import를 하고(Trunk) 이를 checkout으로 branch를 생성하여 작업 후 Merge하는 방식으로 진행

#### Branch 하는 방법

> 1.	Trunk -> branch 클릭
> 2.	To path에 Trunk 외부 level로 경로 설정 & 이름변경가능
