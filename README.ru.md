<div align="center">

# DinoRun - Дино-бег

**Дино-бег - раннер на одной HTML-странице: прыгай через кактусы и пригибайся от птиц. Работает в браузере без сервера и без интернета: откройте `index.html` или играйте онлайн.**

[**▶ Играть онлайн →**](https://alexalesha.github.io/DinoRun/) &nbsp;·&nbsp; [English version of this file](README.md)

[![Status](https://img.shields.io/badge/status-stable-brightgreen)](#) [![CI](https://github.com/ALEXalesha/DinoRun/actions/workflows/ci.yml/badge.svg)](https://github.com/ALEXalesha/DinoRun/actions/workflows/ci.yml) [![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE) [![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML) [![Website](https://img.shields.io/badge/Website-open-0A84FF?logo=googlechrome&logoColor=white)](https://alexalesha.github.io/DinoRun/) [![Built with Claude Code](https://img.shields.io/badge/Built_with-Claude_Code-D97757?logo=claude&logoColor=white)](https://claude.com/claude-code)

Код, тесты и документация этого проекта написаны Claude (Anthropic) в Claude Code. Идеи, проверка и решения - Алексей.

</div>

> Фанатская игра. Не связана с правообладателем игры с динозавриком в известном браузере.

![Меню](docs/screens/menu.png)

![Этап путешествия](docs/screens/play.png)

## Что есть в игре

- **Путешествие:** четыре этапа до финиша на 10 000 м - пустыня, каньон на закате, ночная степь и снежный перевал, с каждым этапом быстрее; начало этапа - контрольная точка.
- **Бесконечный бег:** одна жизнь, день сменяет ночь, скорость растёт; цель - рекорд.
- Птицы летят высоко, средне и низко: под средними пригнуться, через низкие прыгать.
- Достижения и рекорды, настройки с переназначением клавиш, геймпад.
- Спрайты рисуются кодом, звуки и музыка синтезируются WebAudio; ни одного файла из интернета.

## Управление

| Клавиша | Действие |
|---|---|
| Пробел, ↑, щелчок или касание | прыжок (держите - выше) |
| ↓ или S | пригнуться; в прыжке - быстрее вниз |
| Esc | пауза |

Где игра это позволяет, клавиши меняются в настройках.

## Запуск у себя

Откройте `index.html` в Chrome, Edge или Firefox. Всё лежит в репозитории, ничего не скачивается.

## Проверки

Законы - проверки Playwright в `tests/`. Они открывают страницу по файловому адресу в безголовом
Chromium, по одной за раз:

```
npm install
npx playwright install chromium
npm test
```

Захват мыши в проверках всегда поддельный: настоящий `requestPointerLock` в безголовом Chromium
на Windows может зажать курсор пользователя.
Кадры выше сняты в безголовом браузере скриптом кадров сборника Hub.

## История

Игра сделана в сборнике [Hub](https://github.com/ALEXalesha/ALEXalesha.github.io) (папка `web/dino`), там она же работает в Хабе ([играть там](https://alexalesha.github.io/)). Здесь игра лежит вместе с историей коммитов.

## Лицензия

MIT, см. [LICENSE](LICENSE).
