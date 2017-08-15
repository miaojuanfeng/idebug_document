# idebug\_function\_args

功能：遍历函数参数栈，按顺序返回参数栈中的参数值。

声明：

```
/**
* Print function args
*
* @return   array
*/
idebug_function_args();
```

使用：

```
<?php
    function hello($name, $age, $address){
        var_dump(idebug_function_args());
    }
    hello("miaojuanfeng", 20, "Guangzhou");
?>
```

输出：

```
function_args: Args( 'miaojuanfeng' , 20 , 'Guangzhou' )
```

\*未处理：输出参数名

