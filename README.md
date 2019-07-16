# stole
简单的PHP网页采集类，采集网址，匹配内容。
# Composer安装
```Bash
composer require laolei/stole @dev
```
# demo
```php
<?php
require "./vendor/autoload.php";
$st=new Laolei\Stole();
$st->getContent("http://www.deituicms.com/");
$st->cutHtml('<div class="jcList">');
$arr=$st->preg_all('<a href="({url=.*})"[^>]*>({title=.*})</a>');
print_r($arr);
?>
```
# 方法
