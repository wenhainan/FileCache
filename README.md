## filecache
-  轻量级,无依赖的本地文件缓存扩展
## 安装 
```shell
composer require  wenhainan/filecache
```

## 如何使用
```php
use wenhainan\filecache;
//confi. it has a default config.
$config = [
    'expire'=>3600,      //expire time , unit seconds
    'path' =>'./cache'  //self dir
];
$cache = new filecache($config);
//设置缓存 set key cache
$cache->set('key','value',60);   //set key = value  expire = 60s
//获取缓存  get key cache
$cache->get('key');
//删除缓存  delete cache 
$cache->del('key');  
```

## 配置要求
- PHP 5.6+