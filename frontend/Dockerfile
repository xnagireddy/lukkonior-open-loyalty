FROM node:5

RUN apt-get update && apt-get install -y ruby-full rubygems
RUN gem instal sass -v 3.4.2
RUN npm install -g gulp
RUN npm install -g node-sass-x64
RUN npm install -g yarn@1.0.2
COPY . /var/www
WORKDIR /var/www
EXPOSE 3000

CMD npm rebuild node-sass && yarn install && gulp config --prod && gulp compile && gulp prod
