layout: github
title: github pages 及 hexo 创建自己的blog
date: 2016-05-18 15:03:23
tags:
 	- 其它
	- 其它1
---


阮一峰   搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门
http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html

 为什么用github pages

	刚开始折腾 后面方便
 工具

	github 账号一个

  步骤

	 创建一个github pages 规则的仓库 的
	     https://pages.github.com/

上面3步就完成了 github pages 的页面



1. git clone git@github.com:windLemoner/windLemoner.github.io.git  克隆到本地
2. 环境依赖 git node.js  本地装好
3.   安装 hexo npm install -g hexo
4.   部署Hexo hexo init   然后 hexo g        hexo s  可以预览了
5.   其它

		hexo n "我的博客" == hexo new "我的博客" #新建文章
		hexo p == hexo publish
		hexo g == hexo generate#生成
		hexo s == hexo server #启动服务预览
		hexo d == hexo deploy#部署

6.  更换主题


	    找到你需要的主题克隆下来   git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia
		根目录下的 _config.yml         theme 替换为  theme: yilia
		更新主题  cd themes/yilia    git pull


发布到 github  先修改 _config.yml   hexo deploy

	修改根目录下的 _config.yml
	deploy:
	  type: git //typt设为git
	  repository: git@github.com:windLemoner/windLemoner.github.io.git
	  branch: master


	会发现一个错误    Deployer Not Found: git
    npm install hexo-deployer-git --save


//参考知乎
 本地资料丢失后的流程
 git clone git@github.com:windLemoner/windLemoner.github.io.git拷贝仓库（默认分支为hexo）；
  在本地 件夹下通过Git bash依次执行下列指令：npm install hexo、npm install、npm install hexo-deployer-git（记得，不需要**hexo init**这条指令）



end
