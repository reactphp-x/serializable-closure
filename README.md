# ReactphpX SerializableClosure

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## 简介

ReactphpX SerializableClosure 是一个基于 Laravel SerializableClosure 的 PHP 闭包序列化工具，专为 ReactPHP 生态设计。

## 安装

使用 Composer 安装:

```bash
composer require reactphp-x/serializable-closure
```

## 使用示例

```php
use ReactphpX\SerializableClosure\SerializableClosure;

// 序列化闭包
$closure = function() {
    return "Hello World";
};

$serialized = SerializableClosure::serialize($closure);

// 反序列化闭包
$unserialized = SerializableClosure::unserialize($serialized);

echo $unserialized(); // 输出: Hello World

// 使用密钥加密
$secretKey = 'your-secret-key';
$serialized = SerializableClosure::serialize($closure, $secretKey);
$unserialized = SerializableClosure::unserialize($serialized, $secretKey);
```

## 贡献

欢迎提交 Pull Request 或报告问题。

## 许可证

MIT 许可证。详见 [LICENSE](LICENSE) 文件。