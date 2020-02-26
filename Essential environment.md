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
  #follow the steps by:https://docs.docker.com/compose/install/<br>
  #or https://docs.docker.com/compose/install/#alternative-install-options<br>
  以上安装方法会出现安装不完整的问题<br>
  解决方法为先通过以上方法安装，之后去github docker/compose的页面下载，复制到/usr/local/bin<br>
  删除原docker-compose,把下载的文件改名为docker-compose，并使用chmod +x来赋予执行权限<br>
  使用docker-compose version检验安装<br>
## 6.install Hyperledger Fabric(both latest and 1.0.0 are needed & baseos 0.3.1 is needed)
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
  为了方便以后的使用，需要把这几个环境变量添加 profile 文件中（~/.bash_profile 或 /etc/profile）。如果是单用户使用，可以将环境变量添加在 home 目录下的 bash_profile 文件中，如果是多用户使用，需要添加在 /etc/profile 文件。（推荐大家在 /etc/profile 文件中设置环境变量）<br>
  cd<br>
  cd /etc<br>
  sudo gedit profile<br>
  add export GOROOT=/usr/local/go<br>
    export GOPATH=/opt/gopath(前提是fabric的源代码下载到了此处，便将此处作为工作空间了)<br>
    export PATH=$PATH:$GOPATH/bin(使用:添加多个工作目录，当前暂时仅启用一个) at the end of the file<br>
  source profile<br>
  reboot<br>
  use `go env` to check
## 8.每次重启系统或Terminal后先sudo su来获取root权限，随后在去到/etc里面source profile一次，激活go（以后可尝试修改bash_profile来解决每次都要source的问题）  
## 9.下载fabric源码库和fabric-samples
  `cd $GOPATH/src`<br>
  `git clone git://github.com/hyperledger/fabric-samples.git`<br>
  `git clone git://github.com/hyperledger/fabric.git`<br>
## 10.切换源码库分支
  cd到各自目录<br>
  `git checkout release-1.0`<br>
  安装cryptogen, configtxgen, configtxlator<br>
  在.../fabric/common/config目录和/tools目录<br>
  进入到子目录<br>
  `go install`<br>
