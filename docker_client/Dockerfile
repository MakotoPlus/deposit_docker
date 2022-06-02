# ベースイメージを指定
FROM node:16.14.2

USER root
WORKDIR /projects/deposit

#production
ENV NODE_ENV=development
ENV DOCKER_DIR="./docker_client"
ENV SOURCE_DIR="./projects_client/deposit"

#ENV http_proxy 140.227.61.156
#ENV https_proxy 140.227.61.156
#RUN npm -g config set proxy $http_proxy
#RUN npm -g config set https-proxy $https_proxy
#RUN npm -g config set registry "http://registry.npmjs.org/"


RUN apt-get update
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV TERM xterm

#RUN yarn install
RUN apt-get install -y vim less

## コンテナへコピー
#RUN npm config set fetch-retry-mintimeout 500000
#RUN npm config set fetch-retry-maxtimeout 1880000
#COPY $SOURCE_DIR/package.json .
#RUN cd /projects/deposit && npm install
#RUN chmod -R 0777 /projects/deposit/node_modules
#RUN mkdir /projects/deposit/node_modules/.cache
#RUN chmod -R 0777 /projects/deposit/node_modules/.cache

EXPOSE 3000

# ENTRYPOINT [ "yarn", "start" ]
