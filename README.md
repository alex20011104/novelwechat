这是关于微信小程序的小说阅读推荐系统系统的微信前端部分代码。
我将微信阅读系统划分成五个主要的模块，分别是我的书架、书籍详情页、书城中心、个人中心、个性推荐。各个功能模块的具体说明如下：

我的书架：我的书架用来展示用户收藏书籍，书籍按照收藏时间排列，以及跳转书城的链接，方便读者查找喜爱的小说。

书籍详情页：书籍详情页会展示关于这本书籍的诸如书籍名字、封面、作者、简介等这些信息，并提供给用户“收藏”和“立即阅读”还有“评分”的按钮。

点击立即阅读按钮可以立即返回上一次读者看到章节的位置，方便读者阅读不用重新查找目录，书评也是详情页的一大功能，能让用户发表一些对这本书的看法，也可以帮助后来的用户更好的选择自己喜欢的书籍，并提供一个用户交流的平台。

个人中心：在个人中心，用户可以查看自己的个人信息，并选择是否更改它们，还有用户可以查看自己发表的书评和以及评分过的小说，而且还可以查看自己的阅读历史。

个性推荐：在个性推荐模块，用户可以查看系统给自己推荐的小说，并且是按推荐指数降序排列，这推荐功能是系统收集用户的评分信息来推荐的

后台管理页面：对数据库中所有表进行管理，查看小说是否被爬取，爬取时间并且可以选择小说进行爬取。

本项目用到的技术都是基础，并没有高深技术，但是涉及的技术比较多，包括微信小程序原生语言，Django的使用，爬虫技术（Beautifulsoup），推荐算法的设计，numpy的使用，Mysql数据库的设计，包括爬虫怎么批量输入数据库，值得注意的是本系统爬虫爬的是起点中文网。界面设计也是模仿了起点。当然过程也遇到了一些困难，比如小说推荐算法的设计，涉及好几个矩阵的转换，numpy的使用，对于没有接触这方面的新手是具有一定难度的。
还有其他一些小问题，例如爬虫方面，文章段落规范，怎么在爬取，到存入数据库再在微信小程序前端页面保持规范显示，还有一开始进行数据库设计的时候，小说和章节信息应该怎么分表存放，一开始设计错了，最后推翻重新设计。还有在前端的一些同步异步问题，还有设计评论时间的时候，时间戳是在前端还是在后端加，后端orm设计的时候也碰到一些问题，像一运行后自动会在数据库生成表，可能会导致一些同步问题，因为我一开始是在数据库操作软件sqylog里面设计的表，最后发现会和orm的设计里面冲突，导致Django找不到表在哪。
因为写这篇项目介绍的时候已经是完成项目后一年半了，所以有些细节记得不是非常清楚了。

下面的图片是按这个顺序排列的，中间导航栏：小说推荐，分类，排名，全部，然后是搜索，最后是下方导航栏。最后的三张小说管理是使用Django自带的管理系统生成的，代码不在本项目中，本项目只包含微信小程序的前端，后端Django代码在另一个项目仓库：https://github.com/alex20011104/novelDjango.git

![图片1](https://github.com/user-attachments/assets/29ac3789-fd5d-4e3d-b3ff-db52c25ffdce)
![图片2](https://github.com/user-attachments/assets/d607a5ca-c46e-4f48-a781-219195243303)
![图片3](https://github.com/user-attachments/assets/e96a40b3-ffd5-4619-a244-5cf3278283f1)
![图片4](https://github.com/user-attachments/assets/8d4f42d5-cb88-4110-ab65-6db44b93d205)
![图片5](https://github.com/user-attachments/assets/4154d3a6-a4d8-4c0b-91e0-cef387309f90)
![图片6](https://github.com/user-attachments/assets/b655086d-a84f-4df8-8e59-f111acf5afc2)
![图片7](https://github.com/user-attachments/assets/a68e7d64-4a6a-40e8-9e0a-c0c646628804)
![图片8](https://github.com/user-attachments/assets/2051c645-9446-4637-b718-5c29a4630c13)
![图片9](https://github.com/user-attachments/assets/7b52f4bd-cab5-4c7d-ac5c-9d5e3447b028)
![图片10](https://github.com/user-attachments/assets/fa1b1e32-4ec0-4ad4-8297-6a09eba349f1)
![图片11](https://github.com/user-attachments/assets/e6361d47-7121-4bf9-b3bb-63848353d0dd)
![图片12](https://github.com/user-attachments/assets/5781a316-89a2-41cc-9d8e-0db8f517dbb0)
![图片13](https://github.com/user-attachments/assets/b5171b70-437d-41aa-9b85-fc999121ee14)
![图片14](https://github.com/user-attachments/assets/0f2eb500-e69a-45ba-a6cb-08b79abffcf9)
![图片15](https://github.com/user-attachments/assets/87c4bb52-5087-4ba8-8b28-6e96b6ad0b39)
![图片16](https://github.com/user-attachments/assets/e1edc28a-e3e6-4164-9173-67fa02bdfbbb)
![图片17](https://github.com/user-attachments/assets/e853e60f-dde3-4b86-b1cc-deb8caf94ec0)
![图片18](https://github.com/user-attachments/assets/3172195f-c2ba-4f36-8f6b-21d6df245a45)
![图片19](https://github.com/user-attachments/assets/90c6b205-87e4-4ed4-9346-3af506cf147e)
![图片20](https://github.com/user-attachments/assets/7b927357-4013-49aa-8b1d-d226a5e02d44)
