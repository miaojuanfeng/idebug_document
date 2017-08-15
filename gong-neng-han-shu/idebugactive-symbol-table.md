# idebug\_active\_symbol\_table

功能：返回当前符号表中的所有变量，PHP 内核在编译函数或类的成员函数时，会给每个函数分配一个符号表，如果在用户定义的函数内部调用本函数，则会返回该函数所有变量。如果在全局作用域下调用本函数，会返回全局符号表中的所有变量，与 idebug\_symbol\_table 函数相同。

声明：

```
/**
* Print active symbol table
*
* @return   array
*/
idebug_active_symbol_table();
```

使用：

```
<?php
    $g = 120;
    function hello($name){
        $a = "idebug";
        $b = 20;
        var_dump(idebug_active_symbol_table());
    }
    hello("miaojuanfeng");
    var_dump(idebug_active_symbol_table());
?>
```

输出：

```
// 输出当前符号表
array(3) {
    ["name"]=>
    string(12) "miaojuanfeng"
    ["a"]=>
    string(6) "idebug"
    ["b"]=>
    int(20)
}
// 输出全局符号表
active_symbol_table: Array(8) { 
    // 省略内核变量...
    'g' => int(120)
}
```



