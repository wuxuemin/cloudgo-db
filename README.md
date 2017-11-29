## 构建数据服务
#### 一.配置安装好mysql并建立test数据库
![建立测试的数据库:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/test.png)

##### 增加用户 add user

`curl -d "username=ooo&departname=1" http://localhost:8080/service/userinfo`

![-d:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/2.png)

##### 查询用户 query user

`curl http://localhost:8080/service/userinfo?userid=`

![-q:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/chaxun.png)

![-q:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/chaxun2.png)

#### 二.SQL程序测试
+ 启动服务器

`go run main.go`

![启动服务器:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/1.png)

+ 打开另外一个终端

`ab -n 1000 -c 100 http://localhost:8000/?userid=`

![测试:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/cheshi1.png)

![测试:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/cheshi2.png)

#### 三.使用orm库程序测试
+ 启动服务器

`go run main.go`

![启动服务器:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/orm-begin.png)


+ 打开另外一个终端

`ab -n 1000 -c 100 http://localhost:8000/?userid=`

![测试:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/orm-1.png)

![测试:](https://github.com/wuxuemin/cloudgo-db/blob/master/image/orm-2.png)
