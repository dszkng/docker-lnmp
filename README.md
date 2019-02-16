# docker-lnmp

# 目录

- [快速使用](#快速使用)
- [常见问题](#常见问题)



## 快速使用

1. 本地安装`git`、`docker`和`docker-compose`。
2. `clone`项目：
```
$ git clone git@github.com:dszkng/docker-lnmp.git
```
3. 如果不是`root`用户，还需将当前用户加入`docker`用户组：
```
$ sudo gpasswd -a ${USER} docker
```
4. 拷贝环境配置文件`env.example`为`.env`，启动：
```
$ cd docker-lnmp
$ cp env.example .env   # Windows系统请用copy命令，或者用编辑器打开后另存为.env
$ docker-compose up
```
5. 访问在浏览器中访问：

 - [http://localhost](http://localhost)： 默认*http*站点
 - [https://localhost](https://localhost)：自定义证书*https*站点

要修改端口、日志文件位置、以及是否替换source.list文件等，请修改.env文件，然后重新构建：
```
$ docker-compose build php72    # 重建单个服务
$ docker-compose build          # 重建全部服务
```

## 常见问题


参考项目：
[DNMP](https://github.com/yeszao/dnmp)