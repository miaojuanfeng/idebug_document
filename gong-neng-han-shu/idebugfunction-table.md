# idebug\_function\_table

功能：遍历函数符号表，打印输出全部已定义的函数名称。因为内核函数和用户自定义函数都保存在同一张哈希表中，所以打印出的结果包含内核函数和用户自定义函数。

声明：

```
/**
* Print function table
*
* @return   array
*/
idebug_function_table();
```

使用：

```
<?php
    function hello($name){
        $a = "idebug";
        $b = 20;
        idebug_active_symbol_table();
    }
    idebug_function_table();
?>
```

输出：

```
function_table: Array( 
    'zend_version', 
    'func_num_args', 
    'func_get_arg', 
    // 省略其他内核函数...
    'mysqli_affected_rows', 
    'mysqli_autocommit', 
    'mysqli_character_set_name', 
    // 用户自定义函数
    'hello' 
)
```



