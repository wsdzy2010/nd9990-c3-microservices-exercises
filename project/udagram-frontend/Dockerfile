FROM beevelop/ionic AS ionic
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

COPY package*.json ionic.config.json ./

RUN npm ci
COPY . .

## Run
FROM nginx:alpine
#COPY www /usr/share/nginx/html
COPY --from=ionic  /usr/src/app/www /usr/share/nginx/html

