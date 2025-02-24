# 技术栈
* [VuePress](https://vuepress.vuejs.org/zh/)
* markdown

# 开始
* 创建工程`npm init vuepress project-name`
* 运行`npm run docs:dev`

`
发现目录里有个package.json 在vs code里打开会出现debug的按钮，进行调试。是Node.js的机制
`

# 目录分析
* json`a standard file used by Node.js projects`
* js `configuration and layout`
* vue
* markdown
* yml `CI/CD file`

# 当前的状态
* [x] 本地运行
* [x] 配置能够自动化部署
  * `.github\workflows`这个要在根目录
* [x] 删掉了ReadMe, 创建了Index
  * [x] 基于Template格式，进行修改
* [x] 创建新的文章
  * [x] 直接在posts目录下面创建新的文件就能在Article里面找到
* config 里面是主页的信息, plugins部分还没有看明白是怎么工作的
  * 原来就是继承了defineUserConfig
* .vue 文件就很像Django的template 像html

## 已知问题
* Tag 和category里没有数据
  * 有数据，只是被隐藏掉了，调整`.category-wrapper` 就可以了
* 还有其他风格的主题
* push 的时候遇到了拒绝访问的问题，需要把port 换到别处


# 语法分析
## markdown
>Front Matter(yml) + standard Markdown syntax

## YAML
* 数据类型
  * 键值对(字典)
  * 数组`使用 - 开头`

* github action
  * 触发Event`on`
  * 执行的内容`jobs,steps`
    * 使用其他人的actions，以及参数 `uses, with`
    * 执行指令 `run`

# 阅读笔记
* Routing