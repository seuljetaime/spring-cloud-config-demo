# spring-cloud-config-demo



# Config Server

## 初始化git

where `${user.home}/config-repo` is a git repository containing YAML and properties files.

On Windows, you need an extra "/" in the file URL if it is absolute with a drive prefix (for example,`file:///${user.home}/config-repo`).

```
$ cd $HOME
$ mkdir config-repo
$ cd config-repo
$ git init .
$ echo server.port: 8080 > client.properties
$ echo info.foo: bar >> client.properties
$ echo server.port: 8081 > client2-dev.properties
$ echo info.foo: 8081 >> client2-dev.properties
$ git add -A .
$ git commit -m "Add application.properties"
```

## 启动并访问

没有加入spring security，可以直接访问

http://localhost:8888/application/testing

http://localhost:8888/testing/application.yml



**TODO: testing 可以随意输入，用abcd也能看到值**



# Config Client

启动并访问

http://localhost:8080/test

http://localhost:8081/test