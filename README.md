<h1 style="text-align:center">Vue项目实战</h1>

### 安装vue-cli，配置webpack

	npm i vue-cli -global
在该文件夹外面执行下面命令，构建一个vue工程

	vue init webpack my-project

### 项目工程目录介绍
README.md是项目说明文件
package.json项目配置文件，放着很多项目依赖包
package-lock.json是package.json的锁文件，用来确定项目安的第三方包的版本，确保团队编程的统一
license是开源协议的说明
index.html项目默认的首页的模板文件
.postcssrc.js是postcssrc的配置文件
.gitignore提交到git的时候忽略一些文件
.eslintrc.js检查代码规范
.eslintignore忽略检测一些文件
.editorconfig设置了一些编辑器里面的语法
.babelrc用于语法转化
static目录下方的是静态资源
node_modules项目依赖的第三方包
src目录下放的是项目的原代码
src-main.js整个项目的入口文件
src-app.vue项目最原始的根组件
src-router-index.js整个项目的路由都放在这里面
src-components文件夹里面放的是项目的组件
src-assets里面放的是项目中图片类的资源
config放的是项目的配置文件
config-index.js放基础的信息
config-dev.env.js放开发环境的基础信息
config-prod.env.js放生产环境的基础信息
