FROM ubuntu:latest

WORKDIR /usr/src

EXPOSE 5001

COPY . .

RUN apt-get update && apt-get install -y curl && curl -sL https://deb.nodesource.com/setup_16.x | bash && apt install -y nodejs

RUN npm install && npm run build && npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]