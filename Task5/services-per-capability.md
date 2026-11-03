# Сервисы по capability

Таблица: capability → продукт/сервис → владелец → внешняя зависимость.

| Capability | Продукт / сервис | Владелец | Внешняя зависимость |
|---|---|---|---|
| Каталог и контент | Сервис каталога (Go + PostgreSQL) | Backend-команда | — |
| Поиск | Typesense (или Elasticsearch) | Backend | Self-hosted / SaaS |
| Заказы | Сервис заказов (Go + PostgreSQL) | Backend | — |
| Платежи (приём) | Сервис оплаты + Flutterwave/Paystack/M-Pesa | Backend + партнёр | M-Pesa, Flutterwave, Paystack |
| Платежи (выплаты) | Модуль расчётов + провайдер выплат | Backend + CFO | Платёжный провайдер |
| Сверка | Пакетная сверка (cron) | Backend | Отчёты провайдеров |
| Логистика | Интеграция Sendbox/Sendy | Backend | Sendbox, Sendy |
| Отслеживание | Кеш статусов + webhook от перевозчика | Backend | API перевозчиков |
| Онбординг продавцов | WhatsApp Business API + форма | Backend + маркетинг | WhatsApp Business API |
| Кабинет продавца | Web-кабинет (отложен) | Backend | — |
| Покупатели | Сервис аккаунтов + consent-журнал | Backend | — |
| Уведомления | Диспетчер уведомлений + SMS-шлюз | Backend | SMS/USSD-шлюз, FCM/APNs |
| Аналитика | Metabase/Grafana + ETL | Backend/Data | — |
| Безопасность | IAM + KMS + WAF | DevOps | AWS KMS, WAF |
| Платформа | Terraform, GitHub Actions, Prometheus/Grafana | DevOps | — |
