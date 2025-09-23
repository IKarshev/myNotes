[документация](https://docs.github.com/ru/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

Настройки пользователя:
```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

Убрать авторство:
```bash
git commit --amend --reset-author
```

Указать авторство в коммите:
```bash
git commit --author="Ivan Karshev <karshev.ivan09.07.38@gmail.com>" -m "test"
```

### Windows:
```bash
ssh-keygen -t rsa -b 4096 -C "karshev.ivan09.07.38@gmail.com"
```

github->профиль->settings->ssh and GPG keys->add new->вставить публичный ключ
start-ssh-agent.cmd
Добавляем ключ — ssh-add ~/.ssh/<YOUR_GENERATED_RSA_FILE>

linux
	ssh-keygen -t ed25519 -C "karshev.ivan09.07.38@gmail.com"
	github->профиль->settings->ssh and GPG keys->add new->вставить публичный ключ
	включаем ssh — eval `ssh-agent -s`
	Добавляем ключ — ssh-add ~/.ssh/<YOUR_GENERATED_RSA_FILE>

После создания и добавления ключа на git (если до этого не использовался ssh):
	git remote remove origin
	git remote add origin <ссылка "github->code->ssh">