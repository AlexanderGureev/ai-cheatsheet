# ai-cheatsheet

Интерактивная шпаргалка о работе с AI: 3D-сцена на Three.js, тезисы и ссылки на исследования.
Весь сайт — в `index.html`, сборка и установка npm-пакетов не нужны.

## Локальный запуск

Из корня проекта (нужен Python 3):

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Откройте [localhost:8000](http://localhost:8000). Нужен современный браузер с WebGPU или WebGL2
и доступ к интернету для загрузки Three.js и шрифтов.

## Файлы

- `index.html` — интерфейс, стили, 3D-сцена и текст в объекте `CONTENT`.
- `тезисы.md`, `исследования.md` — материалы шпаргалки.
- `examples/a/`, `examples/b/` — прототипы стартового экрана «Синтез» из `llm-aggregator-landing`:
  A «Генезис» и B «Синтез». Локально: [localhost:8000/examples/a/](http://localhost:8000/examples/a/)
  и [localhost:8000/examples/b/](http://localhost:8000/examples/b/).
- `examples/assets/` — общие видео и картинки прототипов, сгенерированные через fal.ai
  (источник каждого файла — в `manifest.json`).

## Деплой

GitHub Actions (`.github/workflows/deploy.yml`) при пуше в `main` публикует на GitHub Pages
`index.html` и папку `examples/`:

- <https://alexandergureev.github.io/ai-cheatsheet/>
- <https://alexandergureev.github.io/ai-cheatsheet/examples/a/>
- <https://alexandergureev.github.io/ai-cheatsheet/examples/b/>
