# idebug\_symbol\_table

功能：输出全局符号表中的所有变量，打印输出结果。

声明：

```
/**
* Print global symbol table
*
* @return   null
*/
idebug_symbol_table();
```

使用：

```
<?php
    $a = "idebug";
    $b = 20;
    idebug_symbol_table(); 
?>
```

输出：

```
symbol_table: Array(7) { 
    // 省略内核变量...
    'a' => string(6) "idebug",
    'b' => int(20)
}
```



