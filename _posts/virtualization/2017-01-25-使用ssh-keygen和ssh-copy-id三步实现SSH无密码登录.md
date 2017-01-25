**ssh-keygen**  产生公钥与私钥对

**ssh-copy-id** 将本机的公钥复制到远程机器的authorized_keys文件中，ssh-copy-id也能让你有到远程机器的home, ~./ssh , 和 ~/.ssh/authorized_keys的权利

*假设，存在HostA和HostB两台Host，那么在HostA上可以执行下列命令进行无密码登录设置。*

1. 在HostA上创建公钥和密钥（一直按Enter）

```
[root@HostA]# ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/jsmith/.ssh/id_rsa):[Enter key]
Enter passphrase (empty for no passphrase): [Press enter key]
Enter same passphrase again: [Pess enter key]
Your identification has been saved in /home/jsmith/.ssh/id_rsa.
Your public key has been saved in /home/jsmith/.ssh/id_rsa.pub.
The key fingerprint is:
33:b3:fe:af:95:95:18:11:31:d5:de:96:2f:f2:35:f9
```

2. 用ssh-copy-id将公钥复制到远程机器中

```
[root@HostB]# ssh-copy-id root@HostB_IP
```

[常见问题](http://blog.chinaunix.net/uid-26284395-id-2949145.html)
