
# 日志

**操作说明**

* 处于中间状态的原生容器实例或原生容器Pod不能执行查看日志操作

* 打印原生容器实例或原生容器Pod中容器的stdout,stderr 标准输出，保存自当前时间起的部分历史日志，日志最大保存容量为10M，超过日志最大保存容量后，历史日志将被自动删除；

* 单次查询日志返回的最大字节数为4K

**原生容器实例操作指南**

1、打开京东云控制台，选择【弹性计算】-【原生容器】-【实例】进入容器列表页；

2、选择需要查看日志的容器，点击操作列的【查看日志】按钮，页面将跳转到详情页的【查看日志】，您也可以在容器的详情页直接选择【查看日志】Tab，查看容器日志；

3、您也可以在【查看日志】输入查询条件，目前支持根据日志输出行数、日志输出时间、最大日志字节对容器日志进行筛选。

**原生容器Pod操作指南**

1、打开京东云控制台，选择【弹性计算】-【原生容器】-【Pod】-【Pod名称】进入Pod详情日志Tab页；

2、选择需要查看日志的容器，点击查询按钮查询指定容器的日志；

3、您也可以设置查询条件，根据查询条件返回对应的容器日志，目前支持根据日志输出行数、时间间隔、最大日志字节数对容器日志进行筛选。
* 日志输出行数：单次请求输出的日志最大行数为4096；
* 最大日志字节数：单次请求输出的日志最大字节数为4KB；
* 时间间隔：设置日志查询的开始时间和结束时间；