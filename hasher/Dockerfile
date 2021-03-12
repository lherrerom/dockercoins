FROM ruby:3.0.0-alpine3.12@sha256:df559e1eb3c1b4884a28caa43ce163425a7f81cf9b7372d33883cf0fea67303f
#RUN apk add --update build-base curl
#Por cada línea de DockerFile se va creando un contenedor, juntamos todos los 
RUN apk add --update build-base && gem install sinatra && gem install thin
#Copia en archivo hasher.rb a la carpeta /  ADD se suele usar para archivos comprimidos, porque al copiarlo se descomprime
#ADD hasher.rb /
COPY hasher.rb /
#Cambiamos el CMD por ENTRYPOINT
ENTRYPOINT ["ruby"]
#CMD ["ruby", "hasher.rb"]
CMD ["hasher.rb"]
EXPOSE 8080
#Si queremos hacer healcheck lo haremos en el yaml del swarm, no aquí
#HEALTHCHECK \
#  --interval=1s --timeout=2s --retries=3 --start-period=1s \
#  CMD curl http://localhost/ || exit 1
