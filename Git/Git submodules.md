Связи подмодулей хранятся в .git/config

Пример добавления подмодуля:
```bash
git submodule add git@github.com:KONTUR-Novosibirsk/kontur.bxcore.git local/modules/kontur.bxcore
```

Установить подмодули:
```bash
git submodule update --init
git submodule update --init --remote --force
```

Удаление подмодуля:
1. Удалить запись о подмодуле в файле .gitmodules
2. Удалить запись о подмодуле в файле .git/config
3. Удалить файлы подмодуля из удаленного репозитория: git rm --cached <path_to_submodule>
4. Удалить запись о подмодуле: rm -rf .git/modules/<path_to_submodule>
5. Удалить не отслеживаемые в данный момент файлы подмодуля: rm -rf <path_to_submodule>