# 环境版本
FROM openjdk:17-jdk-alpine3.14

MAINTAINER yadong.zhang0415@gmail.com

# JVM调优参数等额外参数
ENV PARAMS ""

ENV TZ=PRC

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# 指定容器端口
EXPOSE 8085

# 添加本地 JAR 到容器内
ADD target/blog-admin.jar app.jar

# 容器启动后执行的命令
ENTRYPOINT ["java", "-jar","app.jar" , "-Djava.security.egd=file:/dev/./urandom","$PARAMS"]
