#FROM node:4-slim
FROM node:4-slim@sha256:b5ae41b735cad519ae32cd6eeafbc1191c2d8e9056baf421a17f1c666c2a3753
#RUN npm install express
#RUN npm install redis
RUN npm install express && install redis
COPY files/ /files/
COPY webui.js /
CMD ["node", "webui.js"]
EXPOSE 8080
