# docker-typecho
默认php:8.1-fpm, nginx:latest, PHP环境包含pdo_sqlite 
也可以自行修改docker-compose.yml，typecho.conf变更版本，证书位置，log位置

# 文件夹目录
```
.
├── docker-compose.yml
├── logs
│   └── cer.crt
│   └── key.key
├── nginx
│   └── typecho.conf
└── typecho
```

# 使用方法
``` bash
cd /docker目录
git clone https://github.com/molezz/docker-typecho.git
cd docker-typecho
# 编辑docker-compose.yml 修改端口和版本，放置证书于logs下启用ssl
wget https://github.com/typecho/typecho/releases/download/v1.2.0/typecho.zip
unzip typecho.zip -d typecho && rm typecho.zip
chown -R www-data:www-data typecho/
docker-compose up -d
```
