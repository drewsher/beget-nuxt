# Beget Nuxt.js deploy

Шаблон для деплоя Nuxt-приложения на виртуальный хостинг Beget.ru

## Secrets

- `SSH_PRIVATE_KEY` — приватный ключ
- `REMOTE_HOST` — адрес сервера
- `REMOTE_USER` — имя пользователя
- `TARGET` — путь до папки сайта

Для создания ключа нужно выполнить следующие шаги:

Сгенерируйте ключ: `ssh-keygen -m PEM -t rsa -b 4096`

Сохраните ключ по адресу: `~/.ssh/id_rsa`

Добавьте публичный ключ на сервер: `ssh-copy-id username.beget.tech`

Скопируйте приватный ключ: `cat ~/.ssh/id_rsa`

Добавьте приватный ключ в `Secret Key`

## publicPath

Если проект находится не в корне сайта, тогда в файл `nuxt.config.js` нужно добавить:

```js
router: {
  base: '/path/to/'
}
```
