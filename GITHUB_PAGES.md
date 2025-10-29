# 🚀 Быстрый деплой на GitHub Pages

## Простые шаги:

1. **Создайте репозиторий на GitHub** (например: `flappy-bird-game`)

2. **Закоммитьте и отправьте файлы:**
```bash
git add index.html .gitignore
git commit -m "Add Flappy Bird game"
git remote add origin https://github.com/ВАШ_USERNAME/Название_репозитория.git
git push -u origin main
```

3. **Включите GitHub Pages:**
   - Settings → Pages → Source: `main` branch → Save

4. **Получите URL:**
   ```
   https://ВАШ_USERNAME.github.io/Название_репозитория/
   ```

5. **Обновите `.env`:**
   ```
   WEB_APP_URL=https://ВАШ_USERNAME.github.io/Название_репозитория/
   ```

**Готово!** 🎉 Игра будет доступна по HTTPS URL и работать в Telegram боте.

