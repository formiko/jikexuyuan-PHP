# PHP基本介绍
## PHP的历史
1994年 用Perl创造，后用C重写  
1995年 以Personal Home Tools(PHP Tools)为名发布PHP1和PHP2  
1997年 重写解析器并改称 PHP: Hypertext Preprocessor  
1998年 正式发布PHP3  
1999年 成立 Zend 公司  
2000年 发布PHP4  
2004年 发布PHP5  
## PHP的优点
3. 开发效率高
4. 跨平台
5. 开发部署方便
6. 开源框架丰富：ThinkPHP
7. 开源CMS系统丰富：Joomla、Wordpress
8. 开源网站系统丰富：DiscuzX
## PHP相关的名词
2. Cygmin：在Win模拟Linux环境
3. Apache httpd：Web服务器
4. Nginx：Web服务器，速度快
6. XAMPP：集成开发环境
7. Eclipse PDT
8. ZendStudio
9. PhpStorm
12. SCP：上传下载文件命令
# PHP开发环境搭建
## 开发PHP所需要的集成开发环境
* 软件环境：XAMPP PhpStorm Firefox
## 在Windows平台搭建PHP集成开发环境
安装XAMPP、PhpStorm、Cygwin
# PHP语法基础
## PHP标记符
phptag.php
``` HTML
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Php Tag</title>
</head>
<body>
Hello HTML<br>
<?php
    echo 'Hello PHP';
?>
</body>
</html>
```
## 常量与变量
* 变量
    ``` PHP
        $a = 10;
    ```
* 常量
    ``` PHP
    const THE_VALUE = 100;
    ```
    ``` PHP
    define('THE_VALUE', 100);
    ```
    这两种方法是有区别的
## 函数
``` PHP
function traceNum($a, $b) {
//    echo 'a = ', $a, ' , b = ', $b, '<br>';
    echo "a =$a, b = $b<br>";
}
```
``` PHP
function add($a, $b) {
    return $a + $b;
}
```
## 流程控制
* if else
    ``` PHP
    if($score >= 90) {
        return '优秀';
    } elseif ($score >= 80) {
        return '良好';
    } elseif ($score >= 70) {
        return '好';
    } elseif ($score >= 60) {
        return '可以';
    } else {
        return '差';
    }
    ```
* switch
    ``` PHP
    switch(intval($score/10)) {
        case 10:
        case 9:
            return '优秀';
        case 8:
            return '良好';
        case 7:
            return '好';
        case 6:
            return '可以';
        default:
            return '差';
    }
    ```
## 循环
* for
    ``` PHP
    for($i = 0; $i < 10; $i++ ) {
        echo 'Hello ', $i, '<br>';
    }
    ```
* while
    ``` PHP
    $i = 0;
    while($i < 10) {
        echo 'Hello ', $i, '<br>';
        $i++;
    }
    ```
* do while
    ``` PHP
    $i = 0;
    do{
        echo 'Hello ', $i, '<br>';
        $i++;
    }while($i < 10);
    ```
* break
    ``` PHP
    for($i = 0; $i < 10; $i++ ) {
        echo 'Hello ', $i, '<br>';
        if($i == 5) {
            break;
        }
    }
    ```
* continue
    ``` PHP
    for($i = 0; $i < 10; $i++ ) {
        echo 'Hello ', $i, '<br>';
        if($i == 5) {
            continue;
        }
        echo 'Run here ', $i , '<br>';
    }
    ```
## 逻辑
``` PHP
function traceNum() {
    for($i = 0; $i <= 10; $i++) {
//        if($i % 2 == 0 && $i % 3 == 0) {
//            echo $i, '<br>';
//        }
//        if($i % 2 == 0 || $i % 3 == 0) {
//            echo $i, '<br>';
//        }
        if(!($i%2 == 0)) {
            echo $i, '<br>';
        }
    }
}
traceNum();
```
# PHP常用功能
## PHP字符串
``` PHP
<?php
$str = 'Hello PHP Java C# C++';
echo strpos($str, 'PH');
$str1 = substr($str, 2, 3);
echo $str1;
$result = str_split($str, 2);
print_r($result);
$result = explode(' ', $str);
print_r($result);
$num = 100;
$str2 = $str.'<br>Objective-C '.$num;
echo $str2;
$str2 = "$str<br>Objective-C $num";
echo $str2;
```
