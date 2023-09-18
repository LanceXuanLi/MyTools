FROM ubuntu:22.04

RUN apt-get update &&  apt-get install -y  curl  git  bash  vim  sudo  gnupg  software-properties-common

RUN curl -sL https://deb.nodesource.com/setup_12.x | sed 's/deb.nodesource.com/mirrors.ustc.edu.cn/nodesource/deb/g' | bash - &&     apt-get install -y nodejs

RUN  apt-get install -y openjdk-8-jdk

RUN curl -sL https://golang.google.cn/dl/go1.18.linux-amd64.tar.gz | tar -C /usr/local -xz &&     echo 'export PATH=$PATH:/usr/local/go/bin' >> /root/.bashrc

RUN apt-get install -y python3 python3-pip &&  pip3 install --upgrade pip

RUN apt-get install -y npm

RUN npm install -g cnpm 

RUN bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"

RUN chsh -s /bin/bash root

RUN apt-get clean &&  rm -rf /var/lib/apt/lists/*

WORKDIR /root/work

CMD ["/bin/bash"]
