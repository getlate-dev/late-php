# Late PHP SDK

Official PHP client library for the [Late API](https://docs.getlate.dev) - Schedule and manage social media posts across multiple platforms.

## Requirements

- PHP 8.1 or later

## Installation

```bash
composer require getlate/late-php
```

## Quick Start

```php
<?php
require_once 'vendor/autoload.php';

use Late\Configuration;
use Late\Api\AccountsApi;
use Late\Api\PostsApi;

$config = Configuration::getDefaultConfiguration()
    ->setApiKey('Authorization', 'Bearer YOUR_API_KEY');

// List accounts
$accountsApi = new AccountsApi(null, $config);
$accounts = $accountsApi->listAccounts();
print_r($accounts);

// Create a post
$postsApi = new PostsApi(null, $config);
$post = $postsApi->createPost([
    'content' => 'Hello from PHP!',
    'platforms' => [['platform' => 'twitter', 'accountId' => 'acc_123']],
    'publishNow' => true
]);
```

## Documentation

- [API Reference](https://docs.getlate.dev/api-reference)
- [Getting Started Guide](https://docs.getlate.dev/quickstart)

## License

MIT
