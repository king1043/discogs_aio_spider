
# 基于Asyncio+Aiohttp+Motor+Aio-Pika+Aioredis的国外黑胶唱片信息网站Discogs内容的抓取。
# 使用版本Python3.8


### 项目流程图 
![项目流程图](discogs项目流程图.jpg)


### 安装依赖
```
pip install -r requirements.txt
```
### 如何运行
点击```main.py```运行即可。
注意事项如下:
step1 要先生成任务队列，否则 step2 出错。同理 step3 要等 step2 生成任务队列。
可以根据实际业务情况，优化文件之间的调用。（其中 step1、step2、step3 是函数的别名）
### 代码特点
使用 python 的一些新功能，可以让您学到一些新用法，比如:typing、fstring、pydantic、dataclass
异步编程如何开发，代码之间的调度关系，装饰器的使用等等。
### 存储工具的使用简介
- redis : 去重
- rabbitmq : 利于它的消息确认机制
- mongo : 数据持久化

### 存在的问题
- 在 step1 的时候，使用 step2 和 step3 的方式会报错，所以使用了多进程，后期继续优化，寻找方案。
- pydantic 不能完全替代 dataclass，有些地方会出错，后续调查是否可以解决。
- typing 还有一些没有加，后续补全。

当然水平有限，有很多地方还需要继续优化，欢迎和我来讨论。
### 联系方式
- 微信 : italocxa 
- 公众号 : python学习开发
- 知乎 : https://www.zhihu.com/people/muzico425/columns
- 博客园 : https://www.cnblogs.com/c-x-a/