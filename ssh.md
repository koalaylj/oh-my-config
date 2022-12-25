# ssh

## ssh总自动断开的解决方案
- client
  ```properties
  # /etc/ssh/ssh_config
  TCPKeepAlive yes
  ServerAliveInterval 20 
  ServerAliveCountMax 10
  ```
- server
  ```properties
  # /etc/ssh/ssh_config
  ClientAliveInterval 60
  ClientAliveCountMax 10
  ```

## 记住密码自动登录
- ssh-keygen 生成秘钥对
- ssh-copy-id -i .ssh/id_rsa.pub root@192.168.x.xxx 
- 或者手动把本机~/.ssh/id_rsa.pub 文件内容给append到服务器 ~/.ssh/authorized_key 文件末尾。
