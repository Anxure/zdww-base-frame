# 前端开发规范
## 一、介绍
#### 1.1 介绍
编码规范对于程序员而言尤为首要，有以下几个原因：一个软件的生命周期中，80％的花费在于维护。几乎没有任何一个软件，在其全部生命周期中，均由最初的开辟人员来维护。编码规范可以改良软件的可读性，可以让程序员尽快而彻底地懂得新的代码。
#### 1.2 适用范围
本规范适用于所有前端项目。
#### 1.3 总体原则
简单、易读、易实施执行
## 二、构建项目目录
```
base-frame
├─ mock
├─ public
├─ src
│  ├─ api---------------> 请求方法文件夹
│  ├─ assets-------------> 静态资源文件夹
│  ├─ components---------> 所有公用组件文件夹
│  ├─ config-------------> 全局配置文件
│  ├─ directives---------> 全局指令
│  ├─ filters------------> 全局过滤器
│  ├─ layout-------------> 项目布局layout
│  ├─ main.js------------> 入口文件
│  ├─ mixins-------------> 全局混入
│  ├─ permission.js------> 鉴权文件
│  ├─ plugins------------> 插件文件夹
│  ├─ router-------------> 路由文件夹
│  ├─ store--------------> vuex文件夹
│  ├─ utils--------------> 工具函数文件
│  ├─ App.vue------------> 启动页
│  └─ views--------------> 页面放置文件夹包括页面及组件
├─ tests
├─ .browserslistrc
├─ .editorconfig
├─ .env.development
├─ .env.production
├─ .eslintrc.js
├─ .gitignore
├─ babel.config.js
├─ package-lock.json
├─ package.json
├─ developmentNorm.md
├─ README.md
└─ vue.config.js

```
## 三、命名规范
### （一）文件夹与文件命名
- conponents文件夹里面的文件夹采用大驼峰的形式，其余文件夹采用小驼峰的命名方式
- 所有vue的文件均采用大驼峰的命名方式  例如:AxxxBxxx
- Css文件统一使用kebab-case命名风格
- 属于类的.js文件，除index.js外，使用PascalBase风格，其他类型的.js文件，使用kebab-case风格
### （二）组件的命名
- 组件名应该始终是多个单词的，根组件 App 以及 <transition>、<component> 之类的 Vue 内置组件除外。
- 组件名应该以高级别的 (通常是一般化描述的) 单词开头，以描述性的修饰词结尾。
### （三）代码书写规范
- class命名始终采用kebab-case风格，命名要简洁、明了、有意义。
- Id命名采用小驼峰的方式：例如myStudentCount，命名要简洁、明了、有意义。
- 在模板里面调用组件必须使用kebab-case风格，使用闭合标签，例如：<my-component></my-component>。
- 根据html元素去使用，例如p 元素构造段落, a 元素构造锚点，禁止用行内元素包裹块级标签，最好不要在p标签内嵌套别的标签。
- 设置css样式，禁止使用id选择器，只能采用类选择器。
- 合理使用vue的生命周期，明白不同的生命周期应该做什么事情。
- Js代码书写合理使用空格，统一采用ES6的语法，例如let const，箭头函数，扩展运算符等等，在函数方法中不到万不得已不要改变this的指向，也不要再使用类似于 let _this = this
- 在js代码中，变量的定义也要简单、有意义，禁止使用数字，拼音等，也不要使用无意义的英文，变量使用小驼峰的风格，尽量不定义全局变量，也不要随意定义变量。
- Vuex里面所有的变量名、方法名均采用小驼峰的风格命名。
### （四）组件的书写规范
- 每一个 Vue 组件（等同于模块）首先)必须专注于解决一个单一的问题，独立的、可复用的、微小的 和 可测试的。
- 组件名应该始终是多个单词的，根组件 App 除外，切勿使用保留字；原则：有意义的，简短，可读性。
- 组件的data必须是一个带return的函数。
- props尽可能使用原始类型的数据，且需要指定其类型。
- 为 v-for 设置键值，避免v-if 和 v-for 同时用在同一个元素上，合理使用v-if和v-show。
- 为组件样式设置作用域。
- 组件结构合理，简洁，添加name，name不能HTML元素或者 Vue 保留标签重名。
- 谨慎使用this.$parent，this.$refs。
- 单文件组件文件名的大小写(采用大驼峰)，模板中使用连字符kebab-case。
