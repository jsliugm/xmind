# docker相关

[TOC]

## 安装步骤

### step1：必要的系统工具

```shell
sudo apt-get update
sudo apt-get -y install apt-transport-https ca-certificates curl software-properties-common
```

### step2：安装GPG证书

```shell
curl -fsSL https://mirrors.aliyun.com/docker-ce/linux/ubuntu/gpg | sudo apt-key add -
```

### step3：软件源

```shell
sudo add-apt-repository "deb [arch=amd64] https://mirrors.aliyun.com/docker-ce/linux/ubuntu $(lsb_release -cs) stable"
```

### step4：安装Docker-CE

```shell
sudo apt-get -y update
sudo apt-get -y install docker-ce
```

## docker安装mysql

### 获取官方镜像

```shell
docker pull mysql:5.7
```

### 启动容器

```shell
docker run --name test-mysql -e MYSQL_ROOT_PASSWORD=123 -d mysql:5.7
```

