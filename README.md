# webpack-cli
老司机带你如何快速上车，撸好一个自动化构建工具webpack-cli,这个 适用于webpack，version在4.0+。

##开始
   1.首先安装好node.js，监测node.js的版本。使用命令
   $ node -v 
   $ npm -v 
   测试无误后。进行第二步安装webpack。
   
   2.使用命令行工具或者git bash工具，安装webpack
   $ mkdir xxx 创建一个构建工具的文件夹
   $ npm(cnpm) init  
   初始化项目，其中选项不想填直接enter。
   填完后会得到一个package.json的文件。
   接下来
   $ npm install webpack -g 或者
   $ npm install webpack-cli -g
   $ npm install webpack(webpack-cli) --save-dev
   在安装完成后会得到一个modules的目录。

   3. 在主项目文件夹下面创建一个src的目录文件夹。
   $ mkdir src 
   接下来创建一个index.js的文件。因为在新版本的
   webpack中是以index.js作为文件打包入口。如果没有
   index.js打包会出现报错。
   $ touch index.js

   4. 在package.json文件中scripts选项中加入配置
    "scripts": {  
      "dev": "webpack --mode development",  
      "build": "webpack --mode production"  
               }
     然后使用 
    $ npm run dev (相当于 webpack --mode development )
     或者使用
    $ npm run build(相当于 webpack --mode production)
    得到这开发模式和生产模式两种命令，使用会得到一个dist
    文件目录，得到main.js文件。
    这两种模式的区别会体现在dist出口文件的差异上。
    开发模式出现正常文件编译模式语法。
    生产模式出现文件内容格式非常紧凑，
    适合生产环境下使用。

    5. 最后在index.html中引入main.js就能得到自己想要看到
    的内容了。

    最后总结所有命名行命令：
    $ node -v 
    $ npm -v 
    $ mkdir xxx
    $ npm(cnpm) init 
    $ npm install webpack -g
    $ npm install webpack-cli -g
    $ npm install webpack(webpack-cli) --save-dev
    $ mkdir src 
    $ touch index.js
     "scripts": {  
      "dev": "webpack --mode development",  
      "build": "webpack --mode production"  
               }
    $ npm run dev
    $ npm run build
