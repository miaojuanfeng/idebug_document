# idebug\_function\_call\_stack

功能：遍历函数调用栈，返回当前函数被调用的过程。

声明：

```
/**
* Print function call stack
*
* @return   array
*/
idebug_function_call_stack();
```

使用：

```
<?php
    function f1(){
        f2();
    }
    function f2(){
        f3();
    }
    function f3(){
        f4();
    }
    function f4(){
        var_dump(idebug_function_call_stack());
    }
    f1();
?>
```

输出：

```
function_stack: Stack( 'f1' => 'f2' => 'f3' => 'f4' )
```

函数f1调用了函数f2，函数f2调用了函数f3，函数f3调用了函数f4。

