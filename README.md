## 手机新浪爬虫与ES数据分析的一个样例实现

## 背景

新闻类反爬一般，这是精心挑选的一个站，自底向上的设计方法，从零开始完成一个项目

### 项目目标

* 爬取新浪新闻页，做一个真正的爬虫
* 使用数据库存储并进行数据分析
* 随着数据增长，迁移到ES
* 做一个简单的“新闻搜索引擎
  算法：广度优先算法的一个变体

### 项目的原则

* 【强制】使用GitHub+主干/分支模型进行开发
* 禁止直接pu的master
* 所有的变更通过PR进行
* 【强制】自动化代码质量检查+测试
 * Checkstyle/SpotBugs	
* 最基本的自动化测试覆盖
* 一切工作自动化
* 规范化提交流程

### 项目的设计流程-自底向上

* 单打独斗
* 先实现功能
* 在实现的过程中不停地抽取公用部分
  * 每当你写出很长很啰嗦的代码的时候，就要重构了
  * DRY：每当你复制/粘贴的时候，就要重构了
* 通过重构实现模块化、接口化

### 项目的演进:

* 单线程-> 多线程
* console -> H2 database
* H2 database > Elasticsearch
