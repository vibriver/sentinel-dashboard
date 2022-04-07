本项目是Alibaba Sentinel Dashboard 

## 项目目录

* build：制作 Sentinel Dashboard Docker 镜像的源码
* env: 存放的 docker-compose.yml 需要用到的环境变量
* docker-compose: 适用于编写配置服务（容器）的文件

## Quick Start
* 克隆项目
    ```sh
    git clone https://github.com/ribriver/sentinel-dashboard.git
    ```
* 构建映像
    cd 到 build 目录下
    ```sh
    docker build -t vibrive/sentinel-dashboard:tag .
    ```
* 使用 docker 运行
    ```sh
    docker run -p 8021:8021 -it vibrive/sentinel-dashboard:tag
    ```
* 使用 docker-compose 运行
    cd 根目录
    ```sh
    docker-compose up -d
    ```
* 在浏览器中打开 Sentinel Dashboard 控制台

    link：http://127.0.0.1:8021/

## 常用属性配置

| name                         | description                            | option                         |
| ---------------------------- | -------------------------------------- | ------------------------------ |
| SERVER_PORT                  | server启动的端口                         | 8021                           |
| PROJECT_NAME                 | 项目名称                                 | sentinel-dashboard             |
| USERNAME                     | dashboard登陆用户名                      | 默认sentinel                    |
| PASSWORD                     | dashboard登陆密码                        | 默认sentinel                    |
