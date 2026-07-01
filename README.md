# awesome-meshtastic-ru [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome Meshtastic resources from the Russia/CIS community.

Всё, что создаётся русскоязычным сообществом Meshtastic: прошивки, клиенты, утилиты, железо и сервисы.

---

## Содержание

- [Сервисы и онлайн-инструменты](#сервисы-и-онлайн-инструменты)
- [Прошивки](#прошивки)
- [Клиенты для ПК](#клиенты-для-пк)
- [Интеграции и автоматизация](#интеграции-и-автоматизация)
- [Утилиты и библиотеки](#утилиты-и-библиотеки)
- [Боты и мосты](#боты-и-мосты)
- [Железо и софт](#железо-и-софт)
- [Проекты skrashevich](#проекты-skrashevich)

---

## Сервисы и онлайн-инструменты

- **[Карта Meshtastic Россия](https://map.onemesh.ru)** — Интерактивная карта узлов Meshtastic по России и СНГ (проект ONEmesh). Основана на [liamcottle/meshtastic-map](https://github.com/liamcottle/meshtastic-map). От @vgrishin.

- **[Планировка радиолинков](https://antenna.2tg.dev)** — Инструмент для расчёта и визуализации радиолинков между нодами. Онлайн-калькулятор с учётом рельефа, высоты антенн и частоты. От @ginko_san.

- **[Установщик прошивок (webesptool)](https://github.com/mrekin/webesptool)** — Веб-инструмент для прошивки ESP32-устройств прямо из браузера. Запущен на [flashmesh.ru](https://flashmesh.ru). От @mrekin.

## Прошивки

- **[Сборщик любых прошивок](https://github.com/skrashevich/meshtastic-firmware-builder)** — Go-утилита для кастомной сборки прошивок Meshtastic под любые платы. От @skrashevich.

- **[RU-прошивка на T-Deck/Pager](https://github.com/skrashevich/meshtastic-firmware)** — Полноценная русская раскладка клавиатуры для T-Deck и T-LoRa Pager с переключением EN/RU. Ветка `develop`. От @skrashevich.

  [![T-Deck с русской клавиатурой](https://raw.githubusercontent.com/skrashevich/meshtastic-firmware/develop/.github/screenshot_ru.jpg)](https://github.com/skrashevich/meshtastic-firmware)

- **[Meshtastic+MeshCore прошивка (mesh-loader)](https://github.com/eliahreeves/mesh-loader)** — Прошивка, объединяющая Meshtastic и MeshCore на одном устройстве. От @Dm1ts.

## Клиенты для ПК

- **[MeshRadar](https://github.com/curlysasha/MeshRadar)** — Современный веб-интерфейс для mesh-сети. Поддерживает Serial/TCP подключение, реаль-time сообщения, каналы, DM, traceroute, телеметрию. От @curlysasha.

  [![MeshRadar hero](https://raw.githubusercontent.com/curlysasha/MeshRadar/master/assets/hero.jpg)](https://github.com/curlysasha/MeshRadar)
  [![MeshRadar interface](https://raw.githubusercontent.com/curlysasha/MeshRadar/master/assets/interface.jpg)](https://github.com/curlysasha/MeshRadar)
  [![MeshRadar traceroute](https://raw.githubusercontent.com/curlysasha/MeshRadar/master/assets/traceroute.jpg)](https://github.com/curlysasha/MeshRadar)

- **meshTalk** — Экспериментальный P2P-мессенджер поверх Meshtastic с ACK и авто-поиском портов. Входит в состав [meshTools](https://github.com/peerat/meshTools). От @peerat33.

- **[MeshGo](https://github.com/skobkin/meshgo)** — Десктопный клиент Meshtastic, написанный с помощью Codex. От @skobkin.

- **[MeshApp.ru](https://meshapp.ru)** — Десктопное приложение для Meshtastic и MeshCore: чат, карта нод, настройка радио. Исходный код: [git.privatepractice.app](https://git.privatepractice.app/covox/meshapp). От @coVox.

- **[Консольный клиент (meshtastic_monkey)](https://github.com/mrSatang/meshtastic_monkey)** — Консольный клиент для работы с mesh-сетью. От @Borshchuk.

- **Доработка [MeshSense](https://github.com/Affirmatech/MeshSense)** — Модификация оригинального MeshSense для российских условий. От Алексея Т. *(форк не опубликован)*

- **Клиент на Python+Qt** — Десктопный клиент на Python с Qt-интерфейсом. От @rummind. *(публичный репозиторий не обнаружен)*

- **[Termtastic](https://github.com/acelot/termtastic)** — Функциональный консольный клиент Meshtastic на Rust. От @provaleriy.

## Интеграции и автоматизация

- **[MeshMonitor в Home Assistant](https://github.com/BrainDeLook/meshmonitor-ha)** — Аддон Home Assistant для мониторинга mesh-сети. От @braindelook.

  [![MeshMonitor Logo](https://raw.githubusercontent.com/BrainDeLook/meshmonitor-ha/main/meshmonitor/logo.png)](https://github.com/BrainDeLook/meshmonitor-ha)

## Утилиты и библиотеки

- **[Кодирование кириллицы (MeshCompact)](https://github.com/Eloren1/MeshCompact)** — Замена кириллических символов на ASCII-аналоги для вписывания в лимиты Meshtastic. От @luigivampa92.

- **[Компрессор сообщений (mesh-compressor)](https://github.com/dimapanov/mesh-compressor)** — Сжимает текст в 2–7 раз для отправки в одном 233-байтном пакете Meshtastic. Lossless, 10 языков. От @dimapanov.

  [![Compression by language](https://raw.githubusercontent.com/dimapanov/mesh-compressor/main/docs/img/compression-by-language.png)](https://github.com/dimapanov/mesh-compressor)
  [![Per-language results](https://raw.githubusercontent.com/dimapanov/mesh-compressor/main/docs/img/by-lang-en-ru.png)](https://github.com/dimapanov/mesh-compressor)

- **[TCP/Serial прокси (go-meshtastic-serial2tcp)](https://github.com/skrashevich/go-meshtastic-serial2tcp)** — Go TCP-to-serial bridge для Meshtastic-радио с multi-client доступом, кешированием конфига и mDNS- discovery. От @skrashevich.

  [![Web UI Chat](https://raw.githubusercontent.com/skrashevich/go-meshtastic-serial2tcp/main/docs/webui-chat.png)](https://github.com/skrashevich/go-meshtastic-serial2tcp)
  [![Web UI Channels](https://raw.githubusercontent.com/skrashevich/go-meshtastic-serial2tcp/main/docs/webui-channels.png)](https://github.com/skrashevich/go-meshtastic-serial2tcp)

- **[meshTools](https://github.com/peerat/meshTools)** — Набор Python-утилит: meshLogger (сбор трассировок в SQLite), graphGen (графы топологии), meshTalk (P2P-чат с ACK). От @peerat33.

## Боты и мосты

- **[Бот + лог эфира в Telegram](https://hub.docker.com/r/54ph3r/meshtastic-network-monitor)** — Telegram-бот для мониторинга эфира и отправки сообщений в mesh (Docker-образ). От @s4ph3r.

- **[Бот + эфир в Telegram/Matrix (GoMeshtasticBot)](https://github.com/vakarianplay/GoMeshtasticBot)** — Бот для двусторонней связи Meshtastic ↔ Telegram и Matrix. От @cyberbibki.

- **[Meshtastic Proxy](https://github.com/jf3tt/meshtastic-proxy)** — TCP-прокси для Meshtastic с веб-дашбордом, мультиплексированием клиентов, метриками Prometheus и mDNS. От @jfett.

  [![Web Dashboard](https://raw.githubusercontent.com/jf3tt/meshtastic-proxy/main/screenshots/image.png)](https://github.com/jf3tt/meshtastic-proxy)

- **Бот + эфир в Telegram** — Бот для интеграции Meshtastic с Telegram. От @ginko_san. *(публичный репозиторий не обнаружен)*

- **[Tmesh.ru — связь с Telegram](https://github.com/samfromlv/tmesh)** — Мост между Meshtastic и приватными группами в Telegram. От @alex_shakhov_dev.

- ~~**Blackbox — локальный ИИ** — Локальный AI-ассистент для Meshtastic. От @w3d03.~~ *(автор удалил проект)*

## Железо и софт

- **Плата для nrf52 и E22900m30s** — Кастомная плата на базе nRF52 с модулем E22900m30s для Meshtastic. От @anykey_play. *(публичный репозиторий не обнаружен)*

- **Offgrid-коммуникатор** — Автономное устройство для off-grid связи на Meshtastic. От @dengoroff. *(публичный репозиторий не обнаружен)*

- **Солнечная нода для зонда** — Солнечная автономная нода для метеозонда или полевых условий. От @Tot_i_etot. *(публичный репозиторий не обнаружен)*

## Проекты skrashevich

Дополнительные opensource-проекты от автора списка, не вошедшие в основную подборку:

- **[meshmonitor](https://github.com/skrashevich/meshmonitor)** — Веб-инструмент для мониторинга развёртывания Meshtastic-узлов через TCP/HTTP. Отображает состояние сети, сообщения и телеметрию.

- **[ha-meshtastic](https://github.com/skrashevich/ha-meshtastic)** — Интеграция Meshtastic для Home Assistant (HACS). Позволяет отправлять/получать сообщения, отслеживать ноды и телеметрию прямо из HA.

- **[meshtastic-sniffer](https://github.com/skrashevich/meshtastic-sniffer)** — Широкополосный пассивный приёмник Meshtastic LoRa на SDR с multi-station фьюжном и офлайн-восстановлением PSK.

- **[meshing-around](https://github.com/skrashevich/meshing-around)** — BBS Mesh-скрипты для Meshtastic — организатор почты, пинг-понг бот и справочные системы.

  [![BBS Bot](https://raw.githubusercontent.com/skrashevich/meshing-around/main/etc/pong-bot.jpg)](https://github.com/skrashevich/meshing-around)

- **[openclaw-meshtastic](https://github.com/skrashevich/openclaw-meshtastic)** — Плагин канала Meshtastic для OpenClaw через HTTP, TCP и serial-транспорты.

---

## Добавление проектов

Каталог пополняется. Если вы хотите добавить свой проект — откройте [issue](https://github.com/skrashevich/awesome-meshtastic-ru/issues) или PR.

---

*Составлено по материалам чата [Meshtastic Russia](https://t.me/meshtastic_russia) и [каталога проектов сообщества](https://t.me/meshtastic_russia/346394).*