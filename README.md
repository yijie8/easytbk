# 废弃
本想改写一下变成swoft里能用的，后来发现了另一个也比较好用，建议用这个
https://github.com/Hanson/open-taobao-sdk


git add . && git commit -m 'test' && git push
# 介绍

淘宝联盟、京东联盟、多多进宝SDK封装，有bug或者新增api请提交PR

# 联系方式
微信：bugfixed


# 使用方法
1、安装扩展包

```bash
composer require niugengyun/easytbk
```


2、执行下面的命令，然后修改config/easytbk.php

```bash
php artisan vendor:publish --provider "Yijie\EasyTBK\ServiceProvider"
```

3、淘宝SDK初始化

```php
<?php
use Yijie\EasyTBK\Factory;
use Yijie\EasyTBK\TaoBao\Request\TbkItemInfoGetRequest;

$client = Factory::taobao ();
$req = new TbkItemInfoGetRequest;
$req->setNumIids ($numIids);
return $client->execute ($req);
```

4、京东、拼多多SDK初始化基本一样，自己摸索
