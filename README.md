[![GitHub forks](https://img.shields.io/github/forks/wxxiong6/tree.svg)](https://github.com/wxxiong6/tree/network)
[![Packagist](https://img.shields.io/packagist/v/wxxiong6/tree.svg?style=plastic)]()

php递归无限级树形数据
====  

## 使用使用方法
```PHP
//引入类
include dirname(__DIR__).'/Tree.php';
//数据数组
$data = include __DIR__."/data.php";
//设置主键、parent标识名称 子节点名称
Tree::setConfig($primary = '', $parentId = '', $child = '');
//生成tree
Tree::makeTree($data);
```
运行结果

``` 
Array
(
    [0] = Array
   (
      [id] = 1
       [city] = 中国
       [parent_id] = 0
        [child] = Array
         (
                 [0] = Array
                      (
                             [id] = 2
                            [city] = 北京
                             [parent_id] = 1
                             [child] = Array
                                (
                                 [0] = Array
                                         (
                                             [id] = 3
                                            [city] = 北京市
                                            [parent_id] = 2
                                            [child] = Array
                                                (
                                                   [0] = Array
                                                       (
                                                            [id] = 4
                                                            [city] = 东城区
                                                            [parent_id] = 3
                                                        )

                                                   
                                                )

                                        )

                                )

                        )

                    [1] = Array
                        (
                            [id] = 11
                            [city] = 上海
                            [parent_id] = 1
                            [child] = Array
                                (
                                    [0] = Array
                                        (
                                            [id] = 12
                                            [city] = 上海市
                                            [parent_id] = 11
                                        )


                                )

                        )

                )

        )

)
```
