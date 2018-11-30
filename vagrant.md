Vagrant
----

가상환경을 생성과 관리를 코드로 쉽게 관리 할 수 있게 해주는 Tool

* 설치이유
서버환경이 window 10 이어서 Linux 환경을 사용하기 위해 VM이 필요해서 단순히 virtualbox만 쓰는 것 보다는 vagrant를 사용하여 설정에 문제가 있을경우 os를 재설치하는 경우 효율성을 위해 설치

* Vagrant 설정파일 (Vagrantfile)

```
    Vagrant.configure("2") do |config|
        config.vm.box = "ubuntu/xenial64" --> 이미지는 Box로 명명
        config.vm.provider "virtualbox" do |vb|
        vb.memory = "6144"
        vb.cpus = "6"
       end
      config.vm.network "forwarded_port", guest: 80, host: 8080 --> 포트포워딩
    end
```

* Vagreant 명령어
```
    vagrant status   -> VM 상태 확인
    vagrant ssh 이름 -> 접속 + 이름
    vagrant up       -> VM 설정
    vagrant destroy  -> VM 제거
    vagrant reload   -> 설정 반영
```

*Note*
  서버 안에 Vagrant 위에 VM이 올라가는 형태이기 때문에 VM에 문제가 생겨도 Destroy 하고
  다시 설치하면 되기 때문에 서버에 바로 설치시 오류가 발생 했을 때 서버 OS를
  재설치하는 번거로움을 줄일 수 있음

* Trouble  shooting
  1. vagrant VT-x 오류
      - 부팅메뉴에서 가상화를 킨다
  2. vagrant ssh시 permission denied (window 10)
      - 환경변수 VAGRANT_PREFER_SYSTEM_BIN 값 0 을 추가한다
  3. 외부에서 vagrant vm으로 접속시 permission denied (publickey gssapi-keyex gssapi-with-mic)
      - vm에서 sshd_config 수정 -> PasswordAuthentication yes 변경 -> 재시작
      - [참고](https://blog.naver.com/nniing/221029806232)
