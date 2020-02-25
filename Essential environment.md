# List
## 1.install pip
  $ sudo apt install python-pip
## 2.change the download source of pip
  cd home<br>
  create a new folder named '.pip(2/3)'<br>
  cd /.pip(2/3)<br>
  sudo gedit pip(2/3).conf<br>
  [global]<br>
  index-url = https://pypi.tuna.tsinghua.edu.cn/simple<br>
  [install]<br>
  trusted-host = https://pypi.tuna.tsinghua.edu.cn<br>
  save<br>
  more ~/.pip(2/3)/pip(2/3).conf<br>
## 3.install virtualenv(python)
  pip(2/3) install virtualenv
## 4.install docker
  follow the steps by:https://docs.docker.com/install/linux/docker-ce/ubuntu/
## 5.install docker composer
  follow the steps by:https://docs.docker.com/compose/install/<br>
  or https://docs.docker.com/compose/install/#alternative-install-options<br>
