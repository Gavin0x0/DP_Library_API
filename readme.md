# DP-Library后端部分
## 基于Vue3.0+Eelement-Plus+FastAPI+MongoDB的前后端分离的图书管理的项目「后端部分」
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
 - mongodb「需要新建名为NFTGO的数据库」
## 从零开始
 - 安装Python [下载传送门🚪](https://www.runoob.com/python3/python3-install.html)
 - 命令行「VS code内终端」运行`python -V`，出现版本号「如下图」则可以进行下一步
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx3fsxmvnj609j03emx402.jpg)
 - 检查pip是否正常可用，运行`pip -V`，出现版本号「如下图」则可以进行下一步
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx3gu06x2j60fg0433yn02.jpg)
 - 如果没有pip自行百度安装，直接用anaconda也可以
## 配置镜像
 - pip配置镜像 [配置传送门🚪](https://www.cnblogs.com/jimlau/p/13155747.html)
## 将本项目clone到本地
 - 不会用git也可以直接下载压缩包
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqx3mgdtf1j30pj09mgmp.jpg)
## 用VS code打开项目文件夹
 - ‼️ 重要，确保正确打开项目
 - VS code是以文件夹作为项目的，打开错层级就不能启动项目
## 安装依赖
VS code内终端输入
```
pip install -r requirements.txt
```
## 启动方式
VS code内终端输入
```
python run.py
```
## 简要说明
 - `main.py` 主要代码文件，API接口都写在里面「目前」
 - `models.py` 实体类模型，因为MongoDB的数据结构，需要为其定制特殊的实体类「说实话还没搞太懂」
 - `dbtest.py` 用于数据库连接检测，直接运行该文件，输出系统内全部数据库「如下图」则说明连接成功  
![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqw388oixdj60bu02lgll02.jpg) 
## 特色功能
 - FastAPI会自动生成接口文档，可以直接测试接口，这个功能绝了👍
 - 进入方式：在启动的地址后面加上 `/docs`
 - ![image.png](https://tva1.sinaimg.cn/large/007e6d0Xgy1gqw3fkgh1gj60p10fl0tt02.jpg)