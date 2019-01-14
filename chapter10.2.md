# 前端自动化

### Node.js

Node.js可以理解为是一门后端脚本语言，使用了和JavaScript相同的语法，会使用JavaScript的程序员能很快上手node.js、nodjs在处理高并发方面性能卓越，目前许多公司都在使用nodejs作为后端数据服务和前端开发的中间层。

node.js的中文网站：https://nodejs.org/zh-cn/

## 前端自动化

前端开发的流程越来越复杂，其中有代码的合并和压缩、图片的压缩；对less、sass的预处理；文件操作等，这些工作是重复乏味的，为了优化开发流程，提高工作效率，前端自动化工具就出现了，自动化工具可以通过配置，自动完成这些工作。

## grunt、gulp

grunt和gulp是使用node.js编写的，前端首选的自动化工具，gulp在书写配置上比grunt更简洁，运行的性能更高，gulp逐渐成为主流。

## gulp的使用

gulp使用步骤： 安装nodejs -> 全局安装gulp -> 项目安装gulp以及gulp插件 -> 配置gulpfile.js -> 运行任务 gulp网站：http://gulpjs.com/

常用gulp插件：

压缩js代码（gulp-uglify）

less的编译（gulp-less）

css的压缩 （gulp-minify-css）

自动添加css3前缀（gulp-autoprefixer）

文件改名字 (gulp-rename)