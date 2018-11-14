# ansible一键安装k8s环境

## 配置要求
* 服务器系统为centos7.4以上
* 可以联网
* 主机配置root密码或者免密码登陆
* etcd服务器要求数量大于等于3台,master 1台,worker 2台, 负载均衡1台

## 搭建后的k8s环境说明
* etcd 集群没有tls加密


## 如何运行

1. 在```/roles/common/files/```目录下放入自己的ssh公钥并命名为```id_rsa.pub```,作为以后服务器登陆维护使用
2. 按照```example_hosts```添加服务器ip,并命名为```hosts```
3. 执行```ansible-playbook -i hosts site.yml```
