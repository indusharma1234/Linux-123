FROM nginx
RUN  apt-get update && apt-get install net-tools -y
RUN mkdir /proj
COPY cp -rv /proj/*/usr/share/nginx/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
