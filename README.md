# Vocal Practice Player — GitHub Pages

Публичные документы хранятся отдельно от исходников приложения и локальных черновиков `legal/`.

- `index.html` — главная страница.
- `terms/index.html` — условия и ссылка на стандартное EULA Apple.
- `support/index.html` — поддержка, FAQ и maksim.karonchyk@gmail.com.
- `assets/styles.css` — общие стили без внешних шрифтов, скриптов и аналитики.

## Публикация

Текущий remote: `irakoronchik/vocal-practice-player`. Ожидаемые адреса после публикации:

- https://irakoronchik.github.io/vocal-practice-player/
- https://irakoronchik.github.io/vocal-practice-player/terms/
- https://irakoronchik.github.io/vocal-practice-player/support/

1. В GitHub → Settings → Pages выбрать Source: **GitHub Actions**. Доступность Pages для приватного репозитория зависит от тарифа GitHub.
2. Отправить изменения в `main`. Workflow `.github/workflows/pages.yml` публикует только папку `pages/`. Можно запустить его вручную через Actions.
3. Дождаться успешного deployment и проверить оба публичных URL без авторизации.
4. Указать `/support/` в поле Support URL в App Store Connect. Ссылку `/terms/` можно добавить в описание приложения; лицензия остаётся стандартным EULA Apple.

URL в приложении заданы в `AppLinks` в `VocalPracticePlayer/UI/StudioViews.swift`. При переносе репозитория или подключении домена обновить их одновременно с адресами здесь.

Эти файлы сами по себе не подтверждают включение Pages или успешную публикацию. Политика конфиденциальности остаётся встроенным черновиком в `legal/`: для её публикации ещё нужны сведения, перечисленные в `legal/RELEASE-CHECKLIST.md`.

## Локальный просмотр

Из корня проекта: `python3 -m http.server 8080 --directory pages`, затем открыть http://localhost:8080/. Для проверки ссылки внутри приложения нужен опубликованный HTTPS-сайт.
