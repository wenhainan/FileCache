## filecache
-  轻量级,无依赖的本地文件缓存扩展
## 安装 
```shell
composer require  wenhainan/filecache
```

## 如何使用
```php
use wenhainan\filecache;
//例如 生成一个随机token字符串  这个是自带的一个工具 
$config = [
    'expire'=>3600,      //expire time , unit seconds
    'path' =>'./cache'  //self dir
];
$cache = new filecache();
//设置缓存
$cache->set('key','value',60);   //set key = value  expire = 60s
//获取缓存
$cache->get('key');
//删除缓存
$cache->del('key');  
```

## 配置要求
- PHP 5.6+