# 🐦 Flappy Bird Telegram Mini App

Telegram бот с игрой Flappy Bird на базе библиотеки Aiogram 3.x и веб-приложения.

## ✨ Функциональность

- Telegram Mini App с игрой Flappy Bird
- Команда `/start` - запуск игры с кнопкой веб-приложения
- Команда `/help` - справка
- Полноценная игра Flappy Bird с физикой, счётом и рестартом

## 📦 Установка

1. Установите зависимости:
```bash
pip install -r requirements.txt
```

2. Создайте файл `.env` на основе `.env.example`:
```bash
cp .env.example .env
```

3. Добавьте токен бота в файл `.env`:
```
BOT_TOKEN=ваш_токен_бота
WEB_APP_URL=https://ваш-домен.com/game.html
```

## 🚀 Запуск

### Локальная разработка (с ngrok)

1. Запустите веб-сервер для игры:
```bash
python server.py
```

2. В другом терминале запустите ngrok для создания HTTPS туннеля:
```bash
ngrok http 8000
```

3. Скопируйте HTTPS URL из ngrok (например: `https://abc123.ngrok.io`) и обновите `WEB_APP_URL` в `.env`:
```
WEB_APP_URL=https://abc123.ngrok.io/game.html
```

4. Запустите бота:
```bash
python bot.py
```

5. Откройте бота в Telegram и нажмите `/start`, затем кнопку "🎮 Играть в Flappy Bird"

### Продакшен

1. Загрузите файл `game.html` на любой веб-хостинг с HTTPS поддержкой
2. Обновите `WEB_APP_URL` в `.env` на ваш URL
3. Запустите бота на сервере

## 📁 Структура проекта

- `bot.py` - основной файл бота с обработкой команд
- `game.html` - веб-приложение с игрой Flappy Bird
- `server.py` - простой HTTP сервер для локальной разработки
- `.env` - файл с токеном бота и URL веб-приложения (не коммитится в Git)
- `requirements.txt` - зависимости Python

## 🎮 Управление в игре

- **Клик/Тап** - взлететь
- **Пробел/Стрелка вверх** - взлететь (на клавиатуре)

## ⚠️ Важно

Telegram Mini Apps требуют HTTPS! Для локальной разработки используйте:
- **ngrok** - самый простой способ: `ngrok http 8000`
- **localhost.run** - альтернатива: `ssh -R 80:localhost:8000 localhost.run`
- **Cloudflare Tunnel** - для постоянного туннеля

Для продакшена используйте любой веб-хостинг с HTTPS (GitHub Pages, Netlify, Vercel и т.д.)

