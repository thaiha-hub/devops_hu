# using alpine as the base image
FROM nginx:alpine

RUN apk add --no-cache python3 py3-markdown

COPY README.md /usr/share/nginx/html/README.md

CMD sh -c "markdown_py /usr/share/nginx/html/README.md > /usr/share/nginx/html/index.html && nginx -g 'daemon off;'"

