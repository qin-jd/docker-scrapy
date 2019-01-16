# docker-scrapy

利用docker运行scrapy


### 构建scrapy容器环境
`cd docker`
`docker build -t docker-scrapy .`

### 构建新的scrapy项目
cd到项目根目录 也就是docker-scrapy目录  
`docker run -it --rm  -v "$PWD":/app docker-scrapy scrapy startproject app`

### 启动爬虫
cd到项目根目录 也就是docker-scrapy目录  
`docker run -it --rm  -v "$PWD":/app docker-scrapy scrapy crawl quotes`