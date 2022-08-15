# nginx-config

Запуск:

`docker build -t mynginx .`

`docker run --name nginx-static -v <path-to-repository>/data:/usr/share/nginx/html:ro -v <path-to-repository>/conf:/etc/nginx:ro -p 80:80 --log-driver json-file -d mynginx`

Лог запросов:

`curl --unix-socket /var/run/docker.sock --output <file-to-write> http://localhost:80/containers/<container-id>/logs\?stdout\=1`
