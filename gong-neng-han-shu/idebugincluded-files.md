# idebug\_included\_files

功能：返回当前包含的所有文件。

声明：

```
/**
* Print included files table
*
* @return   array
*/
idebug_included_files();
```

使用：

```
<?php
    require "bug.php";
    var_dump(idebug_included_files());
?>
```

输出：

```
array(2) {
    [0]=>
    string(29) '/home/mjf/Desktop/idebug.php', 
    [1]=>
    string(26) '/home/mjf/Desktop/bug.php' 
)
// idebug.php 是当前脚本文件
```



