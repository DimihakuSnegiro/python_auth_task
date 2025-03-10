# Документация API

## Эндпоинты

- **GET** `http://localhost:8080/docs` - Swagger документация.

- **GET** `http://localhost:8000/auth/login/{provider}`  
  _provider = [yandex, vk]_ — эндпоинт для редиректа на провайдера авторизации.

- **POST** `http://localhost:8000/auth/register` — эндпоинт для регистрации и получения пары токенов.

- **POST** `http://localhost:8000/auth/refresh` — эндпоинт для обновления access токена.

- **GET** `http://localhost:8000/auth/validate` — эндпоинт для валидации токена.

- **GET** `http://localhost:8000/auth/callback/{provider}` — эндпоинты для обратного вызова, которые будут обрабатывать ответы от серверов авторизации.

## Сервисы

- **app** — основной сервис, отвечающий за бизнес-логику авторизации.
- **notifier** — сервис, в фоновом режиме слушающий Kafka.
- **postgres** — база данных для персистентного хранения информации о пользователях.
- **kafka (+ zookeeper)** — сконфигурированный брокер для обеспечения малой связности.

