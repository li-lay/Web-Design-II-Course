FROM nginx:1.27.5-alpine-slim

COPY ./src /usr/share/nginx/html

EXPOSE 80

HEALTHCHECK --interval=10s --timeout=5s --retries=3 \
  CMD curl --fail http://localhost:80 || exit 1

CMD ["nginx", "-g", "daemon off;"]
