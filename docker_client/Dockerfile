# ベースイメージを指定
FROM node:16.14.2

WORKDIR /projects

#production
ENV NODE_ENV=development


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
#RUN npm install create-react-app@4.0.3


EXPOSE 3000

# ENTRYPOINT [ "yarn", "start" ]
