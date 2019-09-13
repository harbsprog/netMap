# netMap

Sistema para gerenciamente e mapeamento de redes, desenvolvido como avaliação da disciplina Projeto Integrado II do Curso de Análise e Desenvolvimento de Sistemas(ADS) do IFSP - Campus Barretos.

## Requirements

Node, Yarn, Database redis and mongo

```shell
Node Install: 
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash 
sudo apt install nodejs
```

```shell
Yarn Install: 
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn
```

Install Redis and MongoDB with docker

```shell
sudo docker run -d --name redis -p 6379:6379 redis
sudo docker run -d --name mongoDB -p 27017:27017 mongo
```
```shell
Create a .env file in the api dir, with the following content
```

```bash
NODE_ENV=development or production
FIRST_LOGIN=1 or 0 (If is a first login use 0 to create a administrative user)
APP_SECRET=YOUR_SECRET_KEY (Set a secret key for token generation)
APP_TTL=YOU_TTL (Set a ttl for token expiration ex: 84600)

DB_URL=YOUR_MONGO_URL

REDIS_HOST=YOUR_HOST_IP
REDIS_PORT=YOUR_HOST_PORT

MAIL_COMPANY=gmail
MAIL_HOST=YOUR_SMTP_HOST
MAIL_PORT=YOUR_SMTP_PORT
MAIL_USER=YOUR_SMTP_USER
MAIL_PASS=YOUR_SMTP_PASS
MAIL_SECURE=false or true
```

## Dependencies

```shell
yarn install
```

## Test

```shell
To start API

cd api
yarn start

----------

To start Frontend

cd frontend
yarn start
```

