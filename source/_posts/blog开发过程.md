# 开发blog过程

## 一.基础逻辑

> 现在本地建立一个网站，然后“发送”出去



## 二.准备步骤：

开发工具：`vscode`

框架：`Hexo`

本地环境：`git`    ，`nodejs`



## 三.开发步骤：

### （一）安装

> 路径：`E:\dutianci\blog`
>
> 右键打开`git bash`：`npm install -g hexo-cli`（完成`hexo`环境的配置）

### （二）初始化网页

1.`hexo init`（`git bash` 下）

![image-20240926103643808](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240926103643808.png)

文件结构：

- public 最终所见网页的所有内容
- node_modules 插件以及hexo所需node.js模块
- _config.yml 站点配置文件，设定一些公开信息等
- package.json 应用程序信息，配置hexo运行所需js包
- scaffolds 模板文件夹，新建文章，会默认包含对应模板内容
- themes 存放主题文件，hexo根据主题生成静态网页（速度贼快）
- source 用于存放用户资源（除 *posts 文件夹，其余命名方式为 “* + 文件名”的文件被忽略）

2.`hexo s` （用vscode打开项目，终端执行）-----完成初步网页的建立

![image-20240926104748650](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240926104748650.png)

### （三）完善网页

1.主题

这里我们介绍下主题和框架，我们现在使用的Hexo是一款快速、简单的博客框架，主题就是开发者根据此框架开发的功能更加完备、页面样式、栏目更多的一种”配件“。就像你用的手机，换上手机壳，选手机壳时需要匹配自己手机的型号，不然也不配套啊是吧

再举个“栗子”，像Android手机（IOS闭源，除非越狱），厂家生产时默认的桌面主题，在主题商店这个app里你能根据自己的喜好选择更好看的图标、背景、字体。就像是“换上新衣”，可以从这个角度理解我们下面要做的操作


2.样式

提及主题，肯定就会有很多啦。还是那句话，大家根据自己的喜好选择就好，这里是[官方主题库](https://hexo.io/themes/)，我比较喜欢**Butterfly**这款主题，下面带大家给自己的网站“换新衣”

- 终端输入：

```
git clone -b master https://gitee.com/immyw/hexo-theme-butterfly.git themes/butterfly
```

- 安装插件：（安装 pug 以及 stylus 的渲染器）

```
npm install hexo-renderer-pug hexo-renderer-stylus --save
```

- 修改配置文件

根目录下找到**_config.yml文件，修改主题为butterfly**
