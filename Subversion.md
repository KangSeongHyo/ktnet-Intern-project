# Subversion(SVN)

설명
----

SCM(Source Code Management)로 Git과 마찬가지로 소스코드 형상관리를 위한 협업 Tool

환경 구성 (Window)
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

Tortoise SVN
------------

SVN 서버에 연결할때 사용

#### Repository 접속하기

> 1.	Tortoise SVN 실행
> 2.	Repository URL 입력 (권한이 있을 경우에만 접속허용)

#### Repository에 Checkout & Commit하기

> 1.	새폴더 생성 후 폴더 내부에서 checkout하면 해당 폴더에 local Repository 생성
> 2.	원하는 폴더 선택 후 왼쪽 클릭 Tortoise SVN -> import
> 3.	message부분에 commit message 작성
> 4.	Ok 하면 Browse에서 볼 수 있음

소스코드 관리
-------------

#### SVN Branch 전략

팀원 한명이 Trunk에 import를 하고 이를 checkout으로 각자 branch를 생성하여 작업 후 Merge 주기에 따라서 Merge하고 버전관리는 Tag 폴더를 두어 진행한.

#### Branch 하는 방법

> 1.	Trunk -> branch 클릭
> 2.	To path에 Trunk 외부 level로 경로 설정 & 이름변경가능
