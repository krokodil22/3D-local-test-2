# 3D Local Editor (GitHub Pages Ready)

Проект полностью подготовлен для публикации как **статический сайт** на GitHub Pages.

## Что уже настроено

- Сборка статической версии фронтенда через Vite.
- Корректные относительные пути к ассетам для GitHub Pages (`VITE_BASE_PATH=./`).
- Автоматический деплой через GitHub Actions (`.github/workflows/deploy-pages.yml`).
- Добавление файла `.nojekyll`, чтобы GitHub Pages не ломал пути к статическим ресурсам.

## Локальный запуск

```bash
npm install
npm run dev
```

## Локальная сборка статической версии

```bash
npm run build:pages
```

Сборка будет в директории `dist/public`.

## Публикация в GitHub Pages

1. Запушьте изменения в ветку `main`.
2. Откройте **Settings → Pages**.
3. В разделе **Build and deployment** выберите **Source: GitHub Actions**.
4. После пуша в `main` workflow `Deploy to GitHub Pages` автоматически соберёт и опубликует сайт.

## Проверка сборки

После `npm run build:pages` можно локально проверить статику, например так:

```bash
npx vite preview --host 0.0.0.0 --port 4173
```

