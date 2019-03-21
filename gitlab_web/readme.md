## 搭建个gitlab

### 根据docker-compose.yml 创建 

```sh
    docker-compose up -d
```
### gitlab.rb 配置


```sh
   cp gitlab.rb.example  config/gitlab.rb
   
   ## gitlab.rb 
    external_url 'http://git.local.com'
        
    ## 邮箱配置--163 邮箱配置为例
    gitlab_rails['gitlab_email_enabled'] = true
    gitlab_rails['gitlab_email_from'] = '邮箱'
    gitlab_rails['smtp_enable'] = true
    gitlab_rails['smtp_address'] = "smtp.163.com"
    gitlab_rails['smtp_port'] = 25
    gitlab_rails['smtp_user_name'] = "邮箱"
    gitlab_rails['smtp_password'] = "邮箱密码"
    gitlab_rails['smtp_domain'] = "smtp.163.com"
    gitlab_rails['smtp_authentication'] = "login"
    gitlab_rails['smtp_enable_starttls_auto'] = true
    gitlab_rails['smtp_tls'] = false
   
```

### 配置虚拟域名
1. 配置nginx地址
    转发一下8081端口
 这里的地址可以自定义
```nginx
  server_name git.local.com
```
2. 配置本地解析
如mac ：
```sh
sudo vi /etc/hosts
## 添加相关的解析
127.0.0.1   git.local.com
```
### 首次登录
首次登陆gitlab，初始化需要等待几分钟，地址才能正常访问。
[git.local.com](http://git.local.com) ,浏览器打开，
首次需要设置root 用户密码，完成。