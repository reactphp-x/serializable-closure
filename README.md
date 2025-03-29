# reactphp-x/serializable-closure

[![License](https://img.shields.io/packagist/l/reactphp-x/serializable-closure.svg)](https://packagist.org/packages/reactphp-x/serializable-closure)

Serializable closures for ReactPHP applications.

## 安装

使用Composer安装:

```bash
composer require reactphp-x/serializable-closure
```

## 使用示例

```php
<?php

require __DIR__ . '/vendor/autoload.php';

use ReactphpX\SerializableClosure\SerializableClosure;

$closure = function() {
    return 'Hello World';
};

$serialized = serialize(new SerializableClosure($closure));
$unserialized = unserialize($serialized);

echo $unserialized(); // 输出: Hello World
```

## 许可证

MIT License (MIT). 请查看[LICENSE](LICENSE)文件获取更多信息。