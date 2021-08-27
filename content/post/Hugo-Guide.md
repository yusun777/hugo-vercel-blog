---
title: "Hugo搭建个人博客"
date: 2021-08-27T00:49:15Z
draft: false
tags: ["hugo","教程","博客"]
categories: ["教程"]
---
**Hugo是一个静态网站生成器，使用Go语言编写，所以他的速度比Hexo快。这就是我选择Hugo的原因。**  
### 安装Hugo
  - Windows  
    	在[Release](https://github.com/gohugoio/hugo/releases)中找到Windows版本下载。  
    	解压之后把`hugo.exe`复制到你想要的地方，并设置PATH。  
  - Linux  
	- Ubuntu/Debian  
        ```sudo apt install hugo```  

    - Arch Linux  
		```sudo pacman -S hugo```  

  - macOS  
	使用Homebrew  
	```brew install hugo```  

### 开始使用
  - 生成博客   
  	  ```hugo new site <site_name> # <site_name>是生成的文件夹名```  
  - 安装主题   
      Hugo没有自带主题，需自己安装。这里我选择了[hugo-theme-even](https://github.com/olOwOlo/hugo-theme-even)主题。  
      ```
      git init
      git submodule add https://github.com/olOwOlo/hugo-theme-even themes/even
      ```  
      复制主题中的样板配置，根据个人喜好修改即可。  
      ```cp themes/even/exampleSite/config.toml .```  
  - 新建文章  
    ```hugo new post/<name>.md # <name>是你文件名```  
  - 生成博客  
  	```hugo --gc -D```  
  - 预览  
  	```hugo server -D```  
	在浏览器输入```localhost:1313```即可预览。
