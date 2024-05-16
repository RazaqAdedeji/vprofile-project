FROM nginx:latest

LABEL Project="Vprofile"
LABEL Author="Razaq"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/nginx.conf.d/vproapp.conf