FROM        docker.io/redhat/ubi9
RUN         dnf install nginx -y 
RUN         rm -rf /usr/share/nginx/html/* 
COPY        index.html /usr/share/nginx/html/index.html
EXPOSE      80 
ENTRYPOINT  ["nginx", "-g", "daemon off;"] 
