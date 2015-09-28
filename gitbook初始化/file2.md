1.  ####gitbook启用本地web服务
    
    在工作区中输入下面的内容：

         gitbook serve ./

    返回下面的信说明服务启动完成，就可访问本地4000端口，来查看文档了：
    
        Live reload server started on port: 35729
        Press CTRL+C to quit ...
        
        info: loading book configuration....OK 
        info: load plugin gitbook-plugin-highlight ....OK 
        info: load plugin gitbook-plugin-livereload ....OK 
        info: >> 2 plugins loaded 
        info: start generation with website generator 
        info: clean website generator
        info: OK 
        info: generation is finished 
        
        Starting server ...
        Serving book on http://localhost:4000

2.  ####gitbook生成本地pdf

    如直接生成pdf就会报错：
    
        gitbook pdf ./
    
    会报告下面的错误：
    
        info: loading book configuration....OK 
        info: load plugin gitbook-plugin-highlight ....OK 
        info: >> 1 plugins loaded 
        info: start generation with pdf generator 
        info: clean pdf generatorOK 
        info: write SUMMARY.html 
        info: start conversion to pdf ....ERROR
        Error: Need to install ebook-convert from Calibre

    从发挥的信息中我们也可以看出，需要安装Calibre这个程序，但这个程序不能使用npm来安装，需要使用apt-get install 来安装,在这个之前需要我们部署一些源：
    
    >it can convert e-books between several formats. It can copy them to your e-reader and so on. 
    >To install Calibre in Ubuntu 13.04, use the following commands:

        sudo add-apt-repository ppa:n-muench/calibre
        sudo apt-get update
        sudo apt-get install calibre

    >Or, if you're using Ubuntu 12.04, use the commands below:

        sudo add-apt-repository ppa:n-muench/calibre2
        sudo apt-get update
        sudo apt-get install calibre
        
如果报错的话，需要查找原因。