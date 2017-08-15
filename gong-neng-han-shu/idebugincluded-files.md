# idebug\_included\_files

功能：返回当前包含的所有文件。

声明：

```
/**
* Print included files table
*
* @return   null
*/
idebug_included_files();
```

使用：

```
<?php
    require "bug.php";
    idebug_included_files();
?>
```

输出：

```
included_files_table: Array( 
    '/home/mjf/Desktop/idebug.php', 
    '/home/mjf/Desktop/bug.php' 
)
// idebug.php 是当前脚本文件
```



