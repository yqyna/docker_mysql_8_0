# docker_mysql_8_0

```
# 创建新用户
 create user 'username'@'host' identified by 'password'; 
# 为用户授权
 grant all privileges on *.* to 'username'@'%' with grant option; 
# 授权之后刷新权限
 flush privileges; 

# 收回权限(不包含赋权权限)
REVOKE ALL PRIVILEGES ON *.* FROM user_name;
REVOKE ALL PRIVILEGES ON user_name.* FROM user_name;
# 收回赋权权限
REVOKE GRANT OPTION ON *.* FROM user_name;
# 操作完后重新刷新权限
flush privileges;
```