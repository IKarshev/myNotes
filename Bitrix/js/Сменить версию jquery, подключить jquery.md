```php
$eventManager = \Bitrix\Main\EventManager::getInstance();
$eventManager->addEventHandler('main', 'OnPageStart', ['EventHandlers\\OnPageStartHandler', 'registerJqueryHandler']);
```


```php
<?php
namespace EventHandlers;

class OnPageStartHandler
{
    public static function registerJqueryHandler()
    {
        $emptyHack = [
            'css' => "",
            'skip_core' => true,
        ];
        \CJSCore::RegisterExt('emptyHack', $emptyHack);
        \CJSCore::Init('emptyHack');
    
        $arJSLib = array(
            'js' => '/bitrix/js/main/jquery/jquery-1.12.4.min.js', 
            'skip_core' => true
        );
        \CJSCore::RegisterExt('jquery', $arJSLib);
    }
}
```

Подключить jquery:
```php
<?CJSCore::Init(['jquery', 'fx']);?>
```