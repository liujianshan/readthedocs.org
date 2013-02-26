生产服务器的配置
=======================================

This document is to help people who are involved in the production instance of Read the Docs running on readthedocs.org. It contains implementation details and useful hints for the people handling operations of the servers.

Servers
-------
The servers are themed somewhere between Norse mythology and Final Fantasy Aeons. I tried to keep them topical, and have some sense of their historical meaning and their purpose in the infrastructure.

域名
~~~~~~

  * readthedocs.com

负载均衡 (nginx)
~~~~~~~~~~~~~~~~~~~~~
    * Asgard

重要文件
```````````````
    * /etc/nginx/sites-enabled/default

重要服务
``````````````````
    * nginx running from init

网络
~~~~~
    * Chimera
    * Asgard

重要文件
```````````````
    * /etc/nginx/sites-enabled/readthedocs
    * /home/docs/sites/readthedocs.org/run/gunicorn.log

重要服务
``````````````````
    * nginx running from init
    * gunicorn (running from supervisord as docs user)

构建
~~~~~
    * Build

重要文件
```````````````
    * /home/docs/sites/readthedocs.org/run/celery.log

重要服务
``````````````````
    * celery (running from supervisord as docs user)

数据库
~~~~~~~~
    * DB

Solr
~~~~
    * DB

Redis
~~~~~
    * DB

网站检测
-------------

``/home/docs/sites/readthedocs.org/checkouts/readthedocs``

Bash 别名
~~~~~~~~~~~~

    * `chk` - Will take you to the checkout directory
    * `run` - Will take you to the run directory

部署
---------

推送代码到服务器. 这是更新代码 & 媒体::

    fab push

重启web服务::

    fab restart

重启构建服务器 celery::

    fab celery


