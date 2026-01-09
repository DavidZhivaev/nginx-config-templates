# Nginx Config Templates

Коллекция полезных шаблонов конфигураций Nginx для разных случаев.

## Структура проекта

- `templates/` — шаблоны конфигов для разных случаев:
  - `static/` — статические сайты
  - `node/` — Node.js / Express приложения
  - `php/` — PHP-FPM / WordPress
  - `ssl/` — HTTPS + SSL
  - `load_balancer/` — Load Balancing
- `scripts/` — вспомогательные скрипты для генерации конфигов
- `README.md` — описание проекта и инструкции
- `LICENSE` — лицензия проекта

## Как использовать

1. Выберите шаблон из папки `templates/`.
2. Скопируйте его в директорию `/etc/nginx/sites-available/`.
3. Отредактируйте `server_name`, пути к файлам и порты.
4. Создайте символическую ссылку в `/etc/nginx/sites-enabled/`:
   ```bash
   sudo ln -s /etc/nginx/sites-available/static_site.conf /etc/nginx/sites-enabled/
