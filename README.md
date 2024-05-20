## filecache
-  轻量级,无依赖的本地文件缓存扩展
## 安装 
```shell
composer require  wenhainan/filecache
```

## 如何使用
```php
use wenhainan\filecache;
//config. it has a default config.
$cache = new filecache();
//设置缓存 set key cache
$cache->set('key','value',60);   //set key = value  expire = 60s
//获取缓存  get key cache
$cache->get('key');
//删除缓存  delete cache 
$cache->del('key');  

```

## 自定义配置
```php
//自定义缓存配置
$config = [
    'expire'=>3600,  //expire time , unit seconds  默认缓存时间，单位秒
    'path' =>'/tmp'  //self dir
];
$cache = new filecache($config);
```

## 配置要求
- PHP 5.6+