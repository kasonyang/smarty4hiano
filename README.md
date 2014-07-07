Smarty4Hiano
=========
Hiano的Smarty模板驱动

特性
=========
本库在Smarty基础上新增了两个标签，用于构建url
* link函数

参数：

`uri`:相对于入口文件(index.php)的路径

示例：`{{link uri="js/jquery.js"}}`

* url函数

参数：

`uri`:动作路径，指向一个动作，可以带参数，格式为`[[MODULE/]CONTROLLER/]ACTION[?PARAM1=PARAM_VALUE1[&PARME2=PARAM_VALUE2&..]]`

示例：`{{url uri="index"}}` `{{url uri="home/index/index?id=1"}}`

模板语法
=========
完全遵循Smarty的语法，有关Smarty的语法请浏览http://www.smarty.net