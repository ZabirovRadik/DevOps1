# DevOps Demo Website

Простой пример того, как Git становится источником правды для всей системы.

## Структура проекта

```
demo-website/
├── index.html      # Основная страница сайта с ракеткой 🚀
├── nginx.conf      # Конфигурация веб-сервера
├── deploy.sh       # Скрипт автоматического развертывания
├── test.sh         # Тестирование ракетки на сайте
├── install-nginx.sh # Скрипт установки nginx
├── install-frp.sh # Скрипт установки и настройки frp
└── README.md       # Документация проекта
```

## Быстрый запуск

1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/ZabirovRadik/DevOps1.git
   cd devops-demo-website
   ```

2. Установите nginx:
   ```bash
   sudo ./install-nginx.sh
   ```
   
3. Установите frp: (токен может измениться!)
   ```bash
   sudo ./install-frp.sh course.prafdin.ru mytoken prafdin
   ```

4. Запустите webhook сервер:
   ```bash
   python3 webhook-server.py
   ```

5. Настройте webhook на GitHub репозиторий: http://webhook.prafdin.course.prafdin.ru/

6. Сайт должен быть доступен по адресу http://app.prafdin.course.prafdin.ru/
