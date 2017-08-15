# idebug\_constant\_table

功能： 返回常量表。

声明：

```
/**
* Print constant table
*
* @return   array
*/
idebug_constant_table();
```

使用：

```
<?php
    define('IDEBUG', 'v123');
    idebug_constant_table();
?>
```

输出：

```
constant_table: Array(574) { 
    'E_ERROR' => int(1), 
    'E_WARNING' => int(2), 
    'E_PARSE' => int(4), 
    'E_NOTICE' => int(8), 
    // 省略其他内核常量...
    'MYSQLI_REPORT_OFF' => int(0), 
    // 用户自定义常量
    'IDEBUG' => string(4) "v123"
}
```



