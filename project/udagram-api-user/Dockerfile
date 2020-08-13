FROM node:11
ENV POSTGRES_USERNAME="du"
ENV POSTGRES_PASSWORD="woaihejia"
ENV POSTGRES_HOST="database-1.cj2gnqzkodlp.us-east-2.rds.amazonaws.com"
ENV POSTGRES_DB="postgres"
ENV AWS_BUCKET="project-195477632629-dev"
ENV AWS_REGION="us-east-2"
ENV AWS_PROFILE="default"
ENV JWT_SECRET="hello"
ENV URL="http://localhost:8100"
WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

CMD ["npm", "run", "prod"]
