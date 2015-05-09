
title: Mac上搭建hexo极简指南
date: 2014-06-05 20:22:31
categories: tools
tags: hexo mac blog
---


1. 安装nvm(node.js的版本管理工具）
	
	```
	$ wget -qO- https://raw.github.com/creationix/nvm/master/install.sh | sh
	```
	
	如果用zsh，需要将最后添加的.bashrc_profile里的那行添加到.zshrc里并重启zsh
2. 安装node.js(通过nvm安装)
	
	```
	$ nvm install 0.10
	```
3. 安装hexo（通过npm安装）

	```
	$ npm install -g hexo
	```

4. 创建hexo文件夹

	```
	$ hexo init hexo
	```
	
5. 本地查看

	输入如下命令后，打开浏览器，并输入`localhost:4000`来查看

	```
	$ hexo g
	$ hexo s
	```

<!--more-->	
6. 注册github账号

7. 创建github账号同名repository

	eg:github账号名位dorayox，则创建`dorayox.github.io` 
	
8. 部署到github上

	执行如下命令：
	
	```
	$ npm install hexo-deployer-git --save
	```

	如下所示编辑_config.yml

	```
	deploy:
	  type: git
	  repository: git@github.com:dorayox/dorayox.github.io.git
	  branch: master
	```
	
	输入如下命令，完成到github得部署，之后打开浏览器并输入`dorayox.github.io`来查看
	
	```
	$ hexo g
	$ hexo d
	```

