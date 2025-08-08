FROM openjdk:8-jre-slim

# 复制本地 jar 文件到镜像中（注意不是从其他阶段）
COPY sentinel-dashboard.jar /home/sentinel-dashboard.jar

ENV JAVA_OPTS="-Dserver.port=8080 -Dcsp.sentinel.dashboard.server=localhost:8080"

EXPOSE 8080

# 使用 JSON 格式 CMD 更规范，防止信号处理问题
CMD java ${JAVA_OPTS} -jar /home/sentinel-dashboard.jar
