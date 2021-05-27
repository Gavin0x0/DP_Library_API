# DP-Library后端部分
## 基于Vue3.0+Eelement-Plus+FastAPI+MongoDB的前后端分离的图书管理项目「后端部分」
## 开发环境
 - 推荐 VS Code [下载传送门🚪](https://www.runoob.com/python3/python3-install.html)
## 开发环境配置「插件推荐」
 - 中文插件
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx36xhwngj60p30frgq102.jpg)
 - 代码高亮
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx39be8w6j60b802zmx802.jpg)
 - 代码格式化
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx3bw7p9yj60b80240sq02.jpg)
## 运行环境
 - python 3.8.5
 - mongodb「需要新建名为DPLibrary的数据库」
## 从零开始
 - 安装Python [下载传送门🚪](https://www.runoob.com/python3/python3-install.html)
 - 命令行「VS code内终端」运行`python -V`，出现版本号「如下图」则可以进行下一步
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx3fsxmvnj609j03emx402.jpg)
 - 检查pip是否正常可用，运行`pip -V`，出现版本号「如下图」则可以进行下一步
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx3gu06x2j60fg0433yn02.jpg)
 - 如果没有pip自行百度安装，直接用anaconda也可以
 - 安装MongoDB数据库 [安装教程传送门🚪](https://www.runoob.com/mongodb/mongodb-window-install.html)
 - 安装Navicat数据库可视化管理工具「非必须」
## 配置数据库
 - 用Navicat连接到本地的MongoDB
 - 创建名为 「DPLibrary」的数据库
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx4322c1xj60hx051gm902.jpg)
 - 数据库内创建一个集合Collection，使得数据库生效
## 配置pip镜像
 - pip配置镜像 [配置传送门🚪](https://www.cnblogs.com/jimlau/p/13155747.html)
## 将本项目clone到本地
 - 不会用git也可以直接下载压缩包
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx3mgdtf1j30pj09mgmp.jpg)
## 用VS code打开项目文件夹
 - ‼️ 重要，确保正确打开项目
 - VS code是以文件夹作为项目的，打开错层级就不能启动项目
## 安装依赖
 - VS code内终端输入
```
pip install -r requirements.txt
```
## 检查数据库连通性
 - VS code内终端输入
```
python dbtest.py
```
 - 输出的数据库里面包含有刚刚创建的 `DPLibrary` 就可以
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx44zwdwdj60ez032jri02.jpg)
## 启动方式
 - VS code内终端输入
```
python run.py
```
 - 如下图则后端启动成功
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx3v5zkkdj60gt05x3z302.jpg)
## That's ALL 🎉
## 简要说明
 - `main.py` 主要代码文件，API接口都写在里面「目前」
 - `models.py` 实体类模型，因为MongoDB的数据结构，需要为其定制特殊的实体类「说实话还没搞太懂」
 - `dbtest.py` 用于数据库连接检测，直接运行该文件，输出系统内全部数据库「如下图」则说明连接成功  
![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqw388oixdj60bu02lgll02.jpg) 
## 特色功能
 - FastAPI会自动生成接口文档，可以直接测试接口，这个功能绝了👍
 - 进入方式：在启动的地址后面加上 `/docs`
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqw3fkgh1gj60p10fl0tt02.jpg)

## 更多资料
### 接口权鉴方面
 - [「关于OAuth2」](https://www.ruanyifeng.com/blog/2019/04/oauth-grant-types.html)
 - [「关于Bearer Token」](https://www.jianshu.com/p/8f7009456abc)
 - [「官方文档中OAuth2的实现」](https://fastapi.tiangolo.com/zh/tutorial/security/simple-oauth2/)
 - [「网友在FastAPI中OAuth2的实现」](https://github.com/MarkShawn2020/oauth2-py)

### 数据库设计方面
 - [「范式与反范式」](https://blog.csdn.net/lein_wang/article/details/53064791)
 - [「MongoDB模式设计」](https://mongoing.com/mongodb-advanced-pattern-design)
 - [关系模型和文档模型的区别在哪里?](https://mongoing.com/mongodb-advanced-pattern-design)  
关系模型需要你把一个数据对象，拆分成零部件，然后存到各个相应的表里，需要的是最后把它拼起来。举例子来说，假设我们要做一个CRM应用，那么要管理客户的基本信息，包括客户名字、地址、电话等。由于每个客户可能有多个电话，那么按照第三范式，我们会把电话号码用单独的一个表来存储，并在显示客户信息的时候通过关联把需要的信息取回来。
而MongoDB的文档模式，与这个模式大不相同。由于我们的存储单位是一个文档，可以支持数组和嵌套文档，所以很多时候你直接用一个这样的文档就可以涵盖这个客户相关的所有个人信息。关系型数据库的关联功能不一定就是它的优势，而是它能够工作的必要条件。 而在MongoDB里面，利用富文档的性质，很多时候，关联是个伪需求，可以通过合理建模来避免做关联。

## 开发规范
 - 接口说明要写清楚
 - 各接口需要层级分明，满足高内聚、低耦合的要求