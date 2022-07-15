# vsftp配置文件及参数说明

## vsftp配置文件及参数说明

/etc/vsftpd目录下文件说明如下：

- /etc/vsftpd/vsftpd.conf是vsftpd的核心配置文件。
- /etc/vsftpd/ftpusers是黑名单文件，此文件中的用户不允许访问FTP服务器。
- /etc/vsftpd/user_list是白名单文件，此文件中的用户允许访问FTP服务器。

配置文件vsftpd.conf参数说明如下：

- 用户登录控制参数说明如下表所示。

  | 参数                 | 说明                      |
  | :------------------- | :------------------------ |
  | anonymous_enable=YES | 接受匿名用户              |
  | no_anon_password=YES | 匿名用户login时不询问口令 |
  | anon_root=（none）   | 匿名用户主目录            |
  | local_enable=YES     | 接受本地用户              |
  | local_root=（none）  | 本地用户主目录            |

- 用户权限控制参数说明如下表所示。

  | 参数                       | 说明                        |
  | :------------------------- | :-------------------------- |
  | write_enable=YES           | 可以上传文件（全局控制）    |
  | local_umask=022            | 本地用户上传的文件权限      |
  | file_open_mode=0666        | 上传文件的权限配合umask使用 |
  | anon_upload_enable=NO      | 匿名用户可以上传文件        |
  | anon_mkdir_write_enable=NO | 匿名用户可以建目录          |
  | anon_other_write_enable=NO | 匿名用户修改删除            |
  | chown_username=lightwiter  | 匿名上传文件所属用户名      |
