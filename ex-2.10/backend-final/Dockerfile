FROM ubuntu:latest

WORKDIR /usr/app
EXPOSE 8000
ENV FRONT_URL=http://localhost:2222

RUN apt-get update && apt-get install -y git && apt-get install -y curl && curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs
RUN git clone https://github.com/docker-hy/backend-example-docker.git .
RUN npm install && npm audit fix

ENTRYPOINT [ "/usr/bin/npm" ]
CMD ["start"]