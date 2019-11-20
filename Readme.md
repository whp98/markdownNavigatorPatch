# 破解markdown Navigator插件

支持正版：本方法只适合穷学生等，如果钱足够请买正版

适用平台：windows 10

IDE：jetbrains全系

本方法适合所有jetbrains产品以安卓studio为例

请使用安装后的jar包来解压适配

首先在你的idea上安装好插件

![](img/破解前.jpg)

然后到

`C:\Users\username\.IntelliJIdea2019.2\config\plugins\idea-multimarkdown\lib
`
提取
`idea-multimarkdown.jar`

新建一个项目文件夹然后在里面新建一个idea文件夹


然后将上面复制的jar包放进去


然后用解压工具解压jar包

`jar xvf idea-multimarkdown.jar`

解压后结构

![](img/解压后.jpg)

之后将jar包删除

建立然后右键将 第一个建立的文件夹用idea打开
新建一个src目录然后右键标记为sources root
 ![](img/标记src.jpg)
然后在其中建包名
`com.vladsch.idea.multimarkdown.license`

建好之后
 ![](img/结构包.jpg)

然后将修改后的文件放到包下，修改后的文件为
[patch/LicenseAgent.java](patch/LicenseAgent.java)


然后配置sdk

 ![](img/sdk.jpg)

选择plugin的选项然后选择要破解的平台安装目录
语言等级和你的jdk一致即可
然后工程下建立编译输出文件夹
 ![](img/插件开发sdk.jpg)
之后配置依赖库
 ![](img/lib配置.jpg)

将你的插件依赖目录填上，配置好后如下：

![](img/目录结构.jpg)

然后将生成的class文件替换掉
markdownNavigator\intellij idea\com\vladsch\idea\multimarkdown\license\LicenseAgent.class
之后就打包
D:\PROject\markdownNavigator\intellij idea>jar cvf idea-multimarkdown.jar *
生成的 jar包直接替换掉原来的后重启idea
破解结果如下
![](img/破解结果.jpg)


# 参考

[破解IDEA插件Markdown Navigator 2.9.7 - 老王的博客](https://wfeil.com/post-79.html)
