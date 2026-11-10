# Database — предварительная схема

## WordPress / MariaDB
Стандартные таблицы WordPress; собственные данные добавлять через плагин и согласованные механизмы WordPress.

## PostgreSQL — News Engine
Предварительные сущности:
- sources
- raw_items
- articles
- article_sources
- processing_jobs
- fact_checks
- duplicate_groups
- ai_generations
- published_posts
- audit_logs

## PostgreSQL — Football Data
Предварительные сущности:
- competitions
- seasons
- teams
- players
- fixtures
- match_events
- match_statistics
- lineups
- standings
- api_sync_logs

## Правила
- Схему уточнить после проверки конкретного API.
- Сохранять внешний provider ID.
- Использовать уникальные ограничения для идемпотентности.
- Хранить время обновления и источник данных.
- Не дублировать без необходимости данные, уже надёжно хранящиеся в WordPress.
