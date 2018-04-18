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
build放项目打包的webpack的一些东西
build-webpack.base.conf.js项目中webpack基础配置项
build-webpack.dev.conf.js项目中webpack开发配置项
build-webpack.prod.conf.js项目中webpack生产配置项

### 单文件组件与Vue中的路由
 文件后缀为.vue的文件，如：app.vue就是单文件组件。
 路由就是根据网址的不同，返回不同的内容给用户。
router-view显示的是当前路由地址所对应的内容
![](https://i.imgur.com/yZdeYbm.jpg)

index.js

	import Vue from 'vue'
	import Router from 'vue-router'
	import Home from '@/pages/home/Home.vue'
	import List from '@/pages/list/List.vue'
	
	Vue.use(Router)
	
	export default new Router({
	  routes: [
	    {
	      path: '/',
	      name: 'Home',
	      component: Home
	    },
	    {
	      path: '/list',
	      name: 'List',
	      component: List
	    }
	  ]
	})

app.vue

	<template>
	  <div id="app">
	    <router-view/>
	  </div>
	</template>
	
	<script>
	export default {
	  name: 'App'
	}
	</script>
	
	<style>
	
	</style>

list.vue

	<template>
	  <div>list</div>
	</template>
	<script>
	export default {
	  name: 'List'
	}
	</script>
	<style>
	
	</style>


### 单页面应用与多页面应用
![](https://i.imgur.com/WvSVc48.jpg)
![](https://i.imgur.com/Vcvs4K9.jpg)

### 项目初始化

1.添加meta标签，属性

	<meta name="viewport" content="width=device-width,initial-scale=1.0,minimum-scale=1.0,maximum-scale=1.0,user-scalable=no">
2.引入reset.css重置样式，覆盖浏览器内置样式，border.css修复高清手机屏幕的多倍屏问题
3.安装fastclick，解决某些浏览器，点击延迟300ms的问题,因为这个功能在开发环境和生产环境都用得着，所以用-S（--save）

	npm i fastclick -S

使用方法,在main.js中输入
	
	import fastClick from 'fastclick'
	fastClick.attach(document.body)

4.iconfont
在iconfont上面新建一个travel项目
5.使用stylus，编写css

	npm i stylus -S
	npm i stylus-loader -S

### header区域开发
1rem= html font-size = 50px
@符号代表src目录

	import '@/assets/styles/reset.css'

在style里面引入的时候要用~@

	@import '~@/assets/styles/varibles.styl'

