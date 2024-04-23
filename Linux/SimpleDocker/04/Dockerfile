FROM nginx
WORKDIR /home/
COPY server/script.sh /home/script.sh
COPY server/server.c /home/
COPY nginx/nginx.conf /etc/nginx/nginx.conf
RUN apt update && apt install -y gcc spawn-fcgi libfcgi-dev
ENTRYPOINT [ "bash", "./script.sh" ]
