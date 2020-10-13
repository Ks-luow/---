#  罗技鼠标宏-多线程框架
**框架本意为帮助更多人学习编写自己的宏**

## 介绍
罗技脚本使用lua语言，并不支持多线程并发，在处理较为复杂的宏脚本时多有不便，故自己写了一个多线程的框架。框架内集成了很多功能，之后会整理汇总，暂时只提供一个基础用法   

***注意！此框架不适用于新版的ghub，请安装旧版lgs!***


## 安装教程
打包下载即可

## 使用说明

1.  将文件下载拆包放到本地，并记录下地址
2.  打开罗技脚本引入框架（路径请使用正斜杠）
```lua
dofile("D:/logic/spring.lua")
```
3.  随意写一个需要运行的函数
```lua
dofile("D:/logic/spring.lua")

function to_do ()
    log("hello world !") -- 框架中集成的输出函数
end
```
4.  把函数放到*init*函数中,用*main*函数将其绑到G4上
```lua
dofile("D:/logic/spring.lua")

function to_do ()
    log("hello world !") -- 框架中集成的输出函数
end

--初始化函数，会在程序开始被调用
function init()  
	main(to_do, 4)--此函数用于将需要执行的方法绑定到键位上
end
```

## 问题反馈
欢迎光临[我的小站](https://luow.fun:88/archives/1/)一起交流学习O(∩_∩)O
