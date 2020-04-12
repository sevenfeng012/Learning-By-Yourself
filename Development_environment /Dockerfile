# 指定基础image
ARG BASE_CONTAINER=jupyter/datascience-notebook
FROM $BASE_CONTAINER

LABEL MAINTAINER sevenfeng012 <343108586@qq.com>


# 添加本地文件夹package到镜像中的/src
ADD ./package/ /src/


# 安装前面添加到镜像/src文件夹中requirements.txt文件中的Python package
RUN \
  cd /src && \
  pip --no-cache-dir install -r requirements.txt && \
  rm -rf /root/.cache