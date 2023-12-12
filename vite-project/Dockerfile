FROM node:slim as build

WORKDIR /app

COPY  package.json .

RUN npm install --silent

RUN npm install react-scripts@3.0.1 -g --silent

COPY . .

RUN npm run build

# Production Stage  

FROM nginx:alpine

COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80

CMD [ "nginx", "-g", "daemon off;" ]
