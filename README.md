# ansible一键安装k8s环境

## 配置要求
* 服务器系统为centos7.4以上
* 可以联网
* 主机配置root免密码登陆
* etcd服务器要求数量大于等于3台,master 1台,worker 大于1台

## 搭建后的k8s环境说明
* k8s版本为1.10.4
* flanneld版本为 v0.10.0
* etcd 版本为 3.3.10 
* etcd 集群没有tls加密

## 验证过的环境
* 阿里云centos7.4

## 如何运行

1. 按照```example_hosts```添加服务器ip,并命名为```hosts```
2. 执行
```
export ANSIBLE_CONFIG=./ansible.cfg
ansible-playbook -i hosts site.yml
```
