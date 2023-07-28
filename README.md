# Проект: meow_book

---

### Описание:

**meow_book** — социальная сеть для обмена фотографиями любимых питомцев. Состоит из бэкенд-приложения на Django и фронтенд-приложения на React. Поддерживает регистрацию и авторизацию, можно добавить нового котика на сайт или изменить существующего, а также просмотреть записи других пользователей.

---


### Как развернуть проект локально:

1. Клонировать репозиторий:
```
	git@github.com:CHEDEIV8/meow_book.git
	cd kittygram\_final/
```
2. Создать в папке kittygram\_final/ файл **.env** с переменными окружения (см. [.env.example](.env.example)).

3. Собрать и запустить докер-контейнеры через Docker Compose:
```
	docker compose up --build
```

---

### Как развернуть проект на серверe:
1. Создать папку kittygram/ с файлом .env в домашней директории сервера (см. [.env.example](.env.example)).
```
	cd ~
	mkdir kittygram
	nano kittygram/.env
```
2. Настроить в nginx перенаправление запросов на порт 9000:
```
    server { 
    	server_name <...>; 
    	server_tokens off;
    	location / { 
    		proxy_pass http://127.0.0.1:9000; 
    	}
    }
```
3. Добавить в GitHub Actions следующие секреты:

    - DOCKER\_USERNAME - логин от Docker Hub

	- DOCKER\_PASSWORD - пароль от Docker Hub

	- SSH\_KEY - закрытый ssh-ключ для подключения к серверу

	- SSH\_PASSPHRASE - passphrase от этого ключа

	- USER - имя пользователя на сервере

	- HOST - IP-адрес сервера

	- TELEGRAM\_TO - ID телеграм-аккаунта для оповещения об успешном деплое

	- TELEGRAM\_TOKEN - токен телеграм-бота

---

### Используемые технологии:

- Python 3.10

- Django

- Django REST Framework

- Node.js
  
- React

- Gunicorn

- Nginx

- Docker

- GitHub Actions

---

### Об авторе

Автор проекта: **Денис Чередниченко**