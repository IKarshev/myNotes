```
/.vscode

/bitrix/catalog_export
/bitrix/backup
/bitrix/cache
/bitrix/crontab
/bitrix/managed_cache
/bitrix/managed_flags
/bitrix/stack_cache
/bitrix/html_pages
/logs
/upload
/local/*.log
/local/*.zip
/local/xlsx
/local/logs

/robots.php
/sitemap.xml
/.htaccess

.idea
.DS_store
/bxapp/vendor
/bxapp/tmp

/*.xml
/*.sql
/*.log
/*.txt
/*.csv

/*.zip
/*.db


/bitrix/themes/.default/modules.css

/bitrix/php_interface/result
/bitrix/tmp
/bitrix/site_checker_*
/bitrix/modules/updater_partner.log
/bitrix/modules/updater.log
/bitrix/.settings_extra.php
/bitrix/err.log
/local/stockInfo.csv

/test*

ssh key
ssh key.pub
.bash_history

restore.php
in.php
copy_infoblock.php

# Для локальных настроек
# Чтобы можно было разворачивать тестовый сайт с другой версией mysql
# Т.к для mysql8.0 требуется убрать innodb_strict_mode в after_connect_d7.php, а для версий младше параметр должен присутствовать
/local/php_interface/dbconn.php
/local/php_interface/after_connect_d7.php
/local/php_interface/after_connect.php
```