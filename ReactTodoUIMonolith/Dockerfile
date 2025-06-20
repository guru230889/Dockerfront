FROM node
WORKDIR /app1
RUN npm install
RUN npm run build
RUN apt-get update && apt-get install -y nginx
RUN cp -r build/* /usr/share/nginx/html
ENTRYPOINT ["nginx", "-g", "daemon off;"]
