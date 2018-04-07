[![Ansible 2.4.3](https://img.shields.io/ansible/role/d/3078.svg)](https://www.ansible.com/)


### 一、摘要

	本roles适用于Ubuntu + Debian

### 二、快速安装nginx

	ansible-playbook -i hlist nginx_install.yml -uroot -k -vv -f30

	-u 指定远程主机执行脚本的账号
	-k 指定上面对应账号的密码
	-vv 显示执行过程中的详情
    -s 通过sudo进行操作

	Note: 如果做了公钥认证的话，可以使用下面的执行方式

	ansible-playbook -i hlist nginx_install.yml -vv -f30 -s


### 三、注意事项

	使用之前一定要修改hlist中的IP为你所需要部署服务的远程机器的IP和sudo密码配置:ansible_sudo_pass='password'

    example:

        [hlist]
        192.168.0.105 ansible_sudo_pass='123456'

	如果场景不同，clone该代码仓库之后，请自行修改../vars/main.yml中的相关信息来满足当前场景的需求


### 四、操作步骤

	如有疑问可以联系@刘宝宝
