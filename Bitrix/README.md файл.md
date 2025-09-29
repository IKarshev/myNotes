```
# {{site name}}

## Процесс установки тестовой копии:

1. Клонировать репозиторий.
2. Скопировать папку `/upload/` с боевого сайта.
3. Создать `.htaccess` в корне сайта.
4. Перенести базу данных с помощью резервного копирования и bitrix скрипта `restore.php` .
5. Создать `/bitrix/.settings_extra.php` и прописать там доступы к базе данных:

\```php
<?php
return array(
  'connections' => array(
    'value' => array(
      'default' => array(
        'className' => '\\Bitrix\\Main\\DB\\MysqliConnection',
        'host' => "",
        'database' => "",
        'login' => "",
        'password' => "",
        'options' => 2,
      ),
    ),
  ),
  'exception_handling' => array(
    'value' => array(
      'debug' => false,
      'log' => array(
        'settings' => array(
          'file' => 'bitrix/err.log',
          'log_size' => 1000000,
        ),
      ),
    )
  ),
  'crypto' =>
    array(
      'value' =>
        array(
          'crypto_key' => '', // уникальный крипто ключ для кукки
        ),
      'readonly' => true,
    ),
);
\```

6. Закрыть сайт от роботов, создав ~/robots.txt

\```bash
User-agent: *
Disallow: /
\```