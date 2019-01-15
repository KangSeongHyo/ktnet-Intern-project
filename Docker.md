# Docker

컨테이너 기반의 가상머신 관리 플랫폼

특징
----

-	server와 client로 구성
-	vagrant 같은 경우 하이퍼바이저 위에서 동작하여 각각 마다 Guest OS 생성
-	Docker는 Engine 위에서 여러 컨테이너를 두어 각각의 어플리케이션이 독립적으로 작동
-	이미지를 통한 컨테이너 구현

사용하는 이유
-------------

문제점
------

-	컨테이너는 VM을 완벽히 대체할 수 없다. 완벽하게 분리하지는 못하기 때문

Docker 명령어
-------------

-	`docker run -it --name [name] /bin/bash`
-	`docker start [name]`
-	`docker attach [name]`
-	`docker run -d -p 3306:3306 -e
	MYSQL_ALLOW_EMPTY_PASSWORD=true --name mysql mysql:5.7`
