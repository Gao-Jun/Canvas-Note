Canvas LMS安装最权威的文档肯定是官方文档。官方文档包括2个，分别是[Quick Start](http://github.com/instructure/canvas-lms/wiki/Quick-Start)和[Production Start](http://github.com/instructure/canvas-lms/wiki/Production-Start)。但从更新频率来说，Production Start有时会落后于实际的部署情况，而Production Start一般能够较好反应当前状态。

以下的部分，可以认为是Production Start的中文简化版

# 操作系统及相关软件

* 操作系统：Debian 9 \(Stretch\)
* 数据库：Postgres 9.6，这里用9.6是因为Debian 9的库里默认是9.6，官方文档用的是9.3。
* ```
  # 安装Postgresql，Debian 9默认Postgres 9.6
  $ sudo apt-get install postgresql

  # 创建一个Postgres账号：canvas，这个账号用来今后连接数据库
  $ sudo -u postgres createuser canvas --no-createdb --no-superuser --no-createrole --pwprompt

  # 创建Canvas LMS使用的数据库。canvas_production, canvas_development分别用于不同的运行环境
  $ sudo -u postgres createdb canvas_production --owner=canvas
  $ sudo -u postgres createdb canvas_development --owner=canvas
  ```
* 各种Ruby软件包的依赖



* 啊



