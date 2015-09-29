#####介绍
>sublime软件以其方便的操作，快捷键的多样性，丰富的插件以及可定制的外观深深吸引一代小码。
>sublime的markdown插件可以在sublime下编辑md文件，编译生成相应的html文件。本文介绍完成这个后还会介绍一下sublime+gitbook。

  1.	插件的安装

    打开sublime text 2，输入`ctrl+alt+p`(package control的安装方式在这里就不介绍了)。
    打开后输入install，就弹出来对话框，在这里输入`markdown preview`，就会显示出相应的包，回车
    确认进行安装。（需要注意的是，安装的时候，sublime需要使用管理员启动）

  2.	配置

  	打开`Preferences`>`Package Settings`>`Markdown Preview`
  	在这里有2个选项，一个默认设置另外一个是user的设置。我们打开`Settings -Default`默认的设置。
  	内容如下：

  	```
	/*
		Markdown Preview default settings
	*/
	{
	/*
		Sets the default opener for HTML files
		default - Use the system default HTML viewer
		other - Set a full path to any executable. ex: /Applications/Google Chrome Canary.app or /Applications/Firefox.app
	*/
		"browser": "/usr/bin/google-chrome-stable",
	```

	配置文件内容很多，拿上面举例，也就是设置浏览器，后面加上浏览器的默认的全路径即可。
	但是我在配置的时候，没有成功，不能自动打开。

  3.	编译

  	输入下面的命令：
  	```
  	ctrl + b
  	```
  	之后会返回下面的信息，说明编译成功：

  		```
  		Compiling /home/cuizz/test/gitbook/mybook/sublime/markdown.md...
        		->/home/cuizz/test/gitbook/mybook/sublime/markdown.html
		[Finished in 0.1s]
  		```

  	这样就编译好了，接下来我们在浏览器中显示。sublime输入快捷键：
  		```
  		ctrl+shift+p
  		```
  	之后输入:`mpp`，也就是`Markdown Preview: Preview in Browser`,这个命令的首字母。
  	之后回车，在弹出的对话框中，选择markdown,这个页面(markdown.html)就会在你设置的浏览器中显示出来了。
  	**需要注意的是，这个插件还不能识别模板信息，因此如果需要操作模板的话，还是需要在gitbook下运行。**

  4.	sublime+gitbook

  	这个结合其实就是将编辑gitbook工程中的编辑器，换成了sublime。加入我们使用gitbook的服务的方式启动
  	(`gitbook serve ./`),每当sublime编辑完成md文件并保存后，gitbook的服务会自动检测这个过程，会重启服务
  	大约10s中后，我们的浏览器会自动刷新，这样新的页面就自动生成了。这个过程比较的麻烦，因为重启服务需要时间，因此
  	如果我们想查看效果，还是使用sublime的Markdown Preview工具来查看，完成一个文档后，统一查看效果会更好。


