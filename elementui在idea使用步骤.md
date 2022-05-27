1: elementui本地引入的方式

(1): 下载vue.js与elementui的依赖

(2): 将下载好的两个资源复制到项目中

![1653603360223](5_27.assets/1653603360223.png)

(3): webapp下新建一个html文件

(4): 将导入的头文件加入到html中

```html
<link rel="stylesheet" href="js/lib-master/theme-chalk/index.css"/>
<script src="js/vue.js" charset="utf-8"></script>
<script src="js/lib-master/index.js" charset="utf-8"></script>

```

(5): 完整html文件为

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
</head>
<body>
<div id="app">
  <el-row>
    <el-button>默认按钮</el-button>
    <el-button type="primary">主要按钮</el-button>
    <el-button type="success">成功按钮</el-button>
    <el-button type="info">信息按钮</el-button>
    <el-button type="warning">警告按钮</el-button>
    <el-button type="danger">危险按钮</el-button>
  </el-row>
 
  <el-row>
    <el-button plain>朴素按钮</el-button>
    <el-button type="primary" plain>主要按钮</el-button>
    <el-button type="success" plain>成功按钮</el-button>
    <el-button type="info" plain>信息按钮</el-button>
    <el-button type="warning" plain>警告按钮</el-button>
    <el-button type="danger" plain>危险按钮</el-button>
  </el-row>
 
  <el-row>
    <el-button round>圆角按钮</el-button>
    <el-button type="primary" round>主要按钮</el-button>
    <el-button type="success" round>成功按钮</el-button>
    <el-button type="info" round>信息按钮</el-button>
    <el-button type="warning" round>警告按钮</el-button>
    <el-button type="danger" round>危险按钮</el-button>
  </el-row>
 
  <el-row>
    <el-button icon="el-icon-search" circle></el-button>
    <el-button type="primary" icon="el-icon-edit" circle></el-button>
    <el-button type="success" icon="el-icon-check" circle></el-button>
    <el-button type="info" icon="el-icon-message" circle></el-button>
    <el-button type="warning" icon="el-icon-star-off" circle></el-button>
    <el-button type="danger" icon="el-icon-delete" circle></el-button>
  </el-row>
</div>
</body>
<link rel="stylesheet" href="js/lib-master/theme-chalk/index.css"/>
<script src="js/vue.js" charset="utf-8"></script>
<script src="js/lib-master/index.js" charset="utf-8"></script>
<script>
  new Vue({
    el: '#app'
  })
</script>
</html>
```

(6): 后面直接改动div标签中的内容即可

(7): 成功组件

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="js/lib-master/theme-chalk/index.css"/>
    <script src="js/vue.js" charset="utf-8"></script>
    <script src="js/lib-master/index.js" charset="utf-8"></script>
</head>
<body>
<div id="app">
    <el-switch
            v-model="value"
            active-color="#13ce66"
            inactive-color="#ff4949">
    </el-switch>
</div>
</body>

<script>
    new Vue({
        el: '#app',
        data() {
            return {
                value: true
            }
        }
    })
</script>
</html>
```

(8): 经验

- 之后在使用elementui不同的组件时，直接在<div></div>组件中改变不同的样式，以及改变不同的data()即可。