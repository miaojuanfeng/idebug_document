# idebug\_class\_table

功能：遍历类符号表，返回全部已定义的类名称。因为内核类和用户自定义类都保存在同一张哈希表中，所以打印出的结果包含内核类和用户自定义类。

声明：

```
/**
* Print class table
*
* @return   array
*/
idebug_class_table();
```

使用：

```
<?php
    class person{
        private $name;
        private $age;
        public function set_name($name){
            $this->name = $name;
        }
        public function set_age($age){
            $this->age = $age;
        }
        public function get_name(){
            return $this->name;
        }
        public function get_age(){
            return $this->age;
        }
    }
    var_dump(idebug_class_table());
?>
```

输出：

```
array(146) {
    [0]=>
    string(9) "stdclass"
    [1]=>
    string(12) "traversable"
    // 省略其他内核类...
    'iteratoraggregate', 
    'iterator', 
    'arrayaccess', 
    // 用户定义类
    'person' 
)
```



