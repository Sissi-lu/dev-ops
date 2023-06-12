# dev-ops

docker container cp Nginx:/etc/nginx/nginx.conf D:/prepare_for_SUST/project/chat_local/dev-ops/nginx/conf
docker container cp Nginx:/etc/nginx/conf.d/default.conf D:/prepare_for_SUST/project/chat_local/dev-ops/nginx/conf/conf.d/defaut.conf
docker container cp Nginx:/usr/share/nginx/html/index.html D:/prepare_for_SUST/project/chat_local/dev-ops/nginx/html


docker run --restart always --name Nginx -d -v \
D:/prepare_for_SUST/project/chat_local/dev-ops/nginx/html:/usr/share/nginx/html \
-v D:/prepare_for_SUST/project/chat_local/dev-ops/nginx/conf/nginx.conf:/etc/nginx/nginx.conf -p 80:80 nginx