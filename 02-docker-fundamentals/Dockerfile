FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html
RUN echo "Image construite avec Dockerfile" > /message-build.txt
CMD ["nginx", "-g", "daemon off;"]

WORKDIR /app
EXPOSE 80
VOLUME /data
ADD index.html /app/page-copie.html
