在本地生成ssh key

```bash
ssh-keygen -t rsa -C "your_email@email.com"
```

会让你输入密码并且确认密码

在github中添加生成的key,位置在~/.ssh/id_rsa.pub

测试连接

```bash
ssh -T git@github.com
```

这时可以使用git clone将github上的项目clone下来了