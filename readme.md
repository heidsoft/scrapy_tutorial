# 爬虫测试

## 爬虫架构
![爬虫架构](https://doc.scrapy.org/en/latest/_images/scrapy_architecture_02.png)


## 爬虫组件

https://doc.scrapy.org/en/latest/topics/architecture.html#scrapy-engine


## 开发状态目录
```
项目结构
(jenkins) ➜  tutorial tree
.
├── build
│   ├── bdist.macosx-10.12-intel
│   └── lib
│       └── tutorial
│           ├── __init__.py
│           ├── items.py
│           ├── middlewares.py
│           ├── pipelines.py
│           ├── settings.py
│           └── spiders
│               ├── __init__.py
│               ├── quotes_spider.py
│               └── stack_spider.py
├── project.egg-info
│   ├── PKG-INFO
│   ├── SOURCES.txt
│   ├── dependency_links.txt
│   ├── entry_points.txt
│   └── top_level.txt
├── readme.md
├── scrapy.cfg
├── setup.py
└── tutorial
    ├── __init__.py
    ├── __init__.pyc
    ├── dbs
    │   ├── default.db
    │   └── tutorial.db
    ├── eggs
    │   └── tutorial
    │       └── 1536139120.egg
    ├── items.json
    ├── items.py
    ├── items.pyc
    ├── logs
    │   └── tutorial
    │       ├── quotes
    │       │   └── 528f7168b0ed11e8a77000909d9aa4ed.log
    │       └── stack
    │           └── 8428aaa3b0ed11e8987500909d9aa4ed.log
    ├── middlewares.py
    ├── pipelines.py
    ├── quotes-1.html
    ├── quotes-2.html
    ├── quotes.json
    ├── settings.py
    ├── settings.pyc
    ├── spiders
    │   ├── __init__.py
    │   ├── __init__.pyc
    │   ├── quotes_spider.py
    │   ├── quotes_spider.pyc
    │   ├── stack_spider.py
    │   └── stack_spider.pyc
    └── twistd.pid
```

## 爬虫开发命令

```
创建项目
scrapy startproject tutorial

部署项目
scrapyd-deploy tutorial

查看爬虫
scrapy list

触发爬虫
curl http://localhost:6800/schedule.json -d project=tutorial -d spider=quotes

curl http://localhost:6800/schedule.json -d project=tutorial -d spider=stack
```

## 参考

（结合mongo作为数据存储爬虫数据）[https://realpython.com/web-scraping-and-crawling-with-scrapy-and-mongodb/]