# Github协作网络可视化

# 一、项目简介

Github协作网络是由多个开发者之间的代码贡献和协作关系构成的。通过分析GitHub上的开发者协作网络，了解项目的社区结构、社区成员之间的协作关系和交互模式，从而更好地理解项目的特点、演化和发展趋势。分析GitHub中的开发者协作网络可以帮助我们深入了解开发者之间的合作关系和协作模式。该大屏包含团队协作关系网络图、团队的开发者价值分布图、团队活跃度排行、团队协作关系指数展示、团队的分类占比图、团队中成员的合作关系图，布局如图1所示。
![_ZQTQTJ_60C~3TR@_25DPO9.jpg](https://s2.loli.net/2023/10/07/PzqCjOcma3lypbh.jpg)

 <center>图1 Github协作网络可视化</center>

# 二、主要功能

## 1. 团队协作网络模块

在本模块中，首先根据团队活跃度的大小将团队分为三个等级，其中以团队为节点，协作关系指数为边，并且节点的大小代表团队规模的大小，边的粗细代表协作关系指数的大小，以此构建团队协作网络。

![image-20231006145847859](https://s2.loli.net/2023/10/06/3tnKwShbFviHVz6.png)

 图2 团队协作网络图

## 2. 开发者价值分布模块

初始化状态下，本模块展示全部团队的开发者价值分布，根据团队中成员的活跃度将开发者划分为'S'、'A'、'B'、'C'、'D'五个等级，统计每个等级的开发者人数，如图3。通过点击团队协作网络图中的团队节点，该模块会展示该团队中的所有成员的开发者价值分布情况，展示每个成员的等级评估，如图4。
![P__W5__0YVE7Y06DXLZKXR6.png](https://s2.loli.net/2023/10/07/T4ScgwjHq2uhQto.png#pic_center)

图3 全部团队的开发者价值分布

![RX76_VYP_6R1@7PBCJ_@F@5.png](https://s2.loli.net/2023/10/07/mnyg1KZspOuWlTi.png)

图4 某团队的开发者价值分布

## 3. 团队活跃度排名模块

初始状态下，该模块展示活跃度top10的团队，包括这些团队的名称，活跃度和团队人数，如图5所示。在点击团队协作网络图中的团队节点后，该模块会展示该团队中成员用户名，活跃度，评级和分数，如图6。

![17_P~_~VW3FFTTAJDF`_BJS.png](https://s2.loli.net/2023/10/07/fkPUz7sXFVKAc9Z.png)

图5 团队活跃度top10展示

![05XM___T~BZ0C6JFJ_ML@B5.png](https://s2.loli.net/2023/10/07/KkHbuoz3YTEDR2a.png)

图6 某团队的成员详情
​                                                                                              

## 4. 团队协作关系指数模块

该模块在初始状态下展示活跃度在'0-300'的团队，通过选择不同的分类展示不同的数据，横纵坐标皆为该分类中团队的名称，通过点击团队协作网络图中的团队节点，此模块会显示该团队与其他团队的协作指数，如图7。

​ ![WG6E_3CEFA_O_MMD_UM7I@H.png](https://s2.loli.net/2023/10/07/KtXWGefiV4jJPYS.png)

​ 图7 团队协作关系指数图
## 5. 团队分类与成员合作关系详情模块

在初始状态下，该模块以饼状图的形式展示所有团队的分类情况，显示每个分类的人数和占比，以及该协作网络团队的总数，如图8。在选择协作网络中的团队节点后，此模块展示所有成员的合作关系详情，其中节点代表用户，边上的数值表示协作关系指数，如图9所示。

​ ![5GHNYY_M__ZS_2PJGV__9CF.png](https://s2.loli.net/2023/10/07/3Y9xOKjF6SVZknC.png)

图8 所有团队分类情况展示                                                                  

![image-20231006112834791](https://s2.loli.net/2023/10/06/buHvyGUeqjiWlxp.png)

图9 某团队成员合作关系详情图                                                                  


# 三、环境及版本说明

* vue 版本 2.6.11
* element-ui 版本 2.15.13
* echarts 版本 5.1.2
* less 版本 3.0.4
* less-loader 版本 5.0.0
* node 版本 16.13.0

# 四、开发相关环境及配置

* 安装 node 环境

* 项目安装

```JavaScript
npm install
```

* 项目运行

```JavaScript
npm run serve
```
* 视频观看地址

https://www.bilibili.com/video/BV1e84y1m73j/?vd_source=799d6d25b9680813fb1b6ce6204e66a0

* 在线演示地址

http://47.120.28.17/


# 五、代码及代码目录结构及代码文件功能说明
* node_modules node模板安装目录
* public 公共目录
  * index.html webpack打包页面模板
  * jquery.min.js 封装了大量js函数和方法的集合
  * links.txt 用户之间的协作关系数据
  * links1.txt 团队之间的协作关系数据
  * user.txt 所有的用户数据
* src 开发文件目录
  * assets 项目静态文件目录
  * img 所有的图片文件
  * utils 封装的js函数和方法
  * Active.vue 团队协作关系指数热力图
  * App1.vue 项目入口文件
  * Grade.vue 团队开发者价值分布图
  * main.js 项目核心文件
* .gitnore 忽略编译生成的中间文件
* babel.config.js babel配置文件
* package-lock.json 模板与模板之间的依赖关系文件
* package.json 项目描述文件
* README.md 项目说明文档
* vue.config.js 进行本地服务器的配置
* yarn.lock 存储安装过程中的重要信息
