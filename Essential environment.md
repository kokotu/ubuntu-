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
## 6.install Hyperledger Fabric
  via https://hub.docker.com/<br>
  search for<br>
  Hyperledger Fabric<br>
  tools<br>
  ca<br>
  orderer<br>
  peer<br>
  baseos<br>
## 7.set go
  cd /usr/local<br>
  wget https://golang.google.cn/dl/......<br>
  tar -xzf ...<br>
  cd go<br>
  bin/go version<br>
  cd<br>
  cd /etc<br>
  sudo gedit profile<br>
  add export GOROOT=/usr/local/go and export PATH=$PATH:$GOROOT/bin:$GOBIN at the end of the file<br>
  source profile<br>
  reboot<br>
  use `go env` to check
  
