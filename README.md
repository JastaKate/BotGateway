# BotGateway

API Gateway для проекта Telegram-бота рецептов. Предназначен для перенаправления HTTP-запросов к TgRecipeBot, BreakfastsService и DinnerService через единый адрес

## Маршруты

В конфигурации заданы направления:

- `/bot/**` → TgRecipeBot, по умолчанию `http://localhost:8093`.
- `/api/**` → BreakfastsService, по умолчанию `http://localhost:8092`.
- `/v2/api/**` → DinnerService, по умолчанию `http://localhost:8091`.

Адреса сервисов можно переопределить через переменные окружения `BOT_ROUTE_URI`, `BR_ROUTE_URI` и `DIN_ROUTE_URI`

## Технологии

Java 21, Spring Boot, Spring Cloud Gateway MVC, Spring Boot Actuator, Gradle

## Запуск

1. Установить JDK 21
2. Запустить сервисы, к которым требуется доступ через Gateway
3. При необходимости задать их адреса через переменные окружения
4. Запустить Gateway.

По умолчанию приложение использует порт `8090`
