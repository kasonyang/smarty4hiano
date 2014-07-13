Smarty4Hiano
=========
Hiano的Smarty模板驱动

特性
=========
本库在Smarty基础上新增了3个标签
* link函数

    作用：生成资源文件的链接

    参数：

    `uri`:相对于入口文件(index.php)的路径

    示例：`{{link uri="js/jquery.js"}}`

* url函数

    作用：生成动作的链接

    参数：

    `uri`:动作路径，指向一个动作，可以带参数，格式为`[[MODULE/]CONTROLLER/]ACTION[?PARAM1=PARAM_VALUE1[&PARME2=PARAM_VALUE2&..]]`

    示例：`{{url uri="index"}}` `{{url uri="home/index/index?id=1"}}`

* form块函数

    作用：自动添加隐藏域`_csrftoken`,防止CSRF攻击

    参数：

    支持任何参数，所有参数将直接转换成<form>的属性

    示例：`{{form method="post"}}{{/form}}` 输出html结果：`<form method="post"><input type="hidden" name="_csrftoken" value="xxxxx"></form>`

模板语法
=========
完全遵循Smarty的语法，有关Smarty的语法请浏览http://www.smarty.net