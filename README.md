# Awesome Meshtastic RU [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Кураторский список проектов, связанных с [Meshtastic](https://meshtastic.org), от русскоязычных разработчиков.  
> A curated list of [Meshtastic](https://meshtastic.org)-related projects from Russian-speaking / CIS developers.

[Meshtastic](https://meshtastic.org) — это проект с открытым исходным кодом, позволяющий использовать недорогие LoRa-устройства для создания децентрализованных mesh-сетей с шифрованием.

---

## Содержание / Contents

- [Прошивки / Firmware](#прошивки--firmware)
- [UI-библиотеки / UI Libraries](#ui-библиотеки--ui-libraries)
- [Клиенты / Desktop & Console Clients](#клиенты--desktop--console-clients)
- [Инструменты / Tools](#инструменты--tools)
- [Инфраструктура / Infrastructure](#инфраструктура--infrastructure)
- [Карты / Maps](#карты--maps)
- [Сборщики / Build Tools](#сборщики--build-tools)
- [Сообщество / Community](#сообщество--community)

---

## Прошивки / Firmware

- **[skrashevich/meshtastic-firmware](https://github.com/skrashevich/meshtastic-firmware)** — Форк официальной прошивки Meshtastic с поддержкой русского языка. Включает: кириллический OLED-дисплей (флаг `OLED_RU`), полную русскую раскладку клавиатуры для T-Deck с переключением EN/RU (Shift+Mic), загрузку онлайн-тайлов карт при наличии Wi-Fi.  
  *Fork of the official Meshtastic firmware with Russian language support: Cyrillic OLED display, Russian keyboard for T-Deck (EN/RU switching via Shift+Mic), online map tile loading over Wi-Fi.*  
  `C++` · Темы: `meshtastic`, `t-deck` · Лицензия: GPL-3.0

---

## UI-библиотеки / UI Libraries

- **[skrashevich/device-ui](https://github.com/skrashevich/device-ui)** — Форк библиотеки [meshtastic/device-ui](https://github.com/meshtastic/device-ui) для TFT и OLED-экранов. Добавляет: загрузку онлайн-тайлов карт по WLAN/HTTPS (OpenStreetMap), русскую виртуальную клавиатуру для T-Deck с аппаратной поддержкой кирилличных символов, переключение RU/EN раскладки.  
  *Fork of meshtastic/device-ui with online OSM tile loading over WLAN/HTTPS, Russian virtual/hardware keyboard for T-Deck, and Cyrillic RU/EN layout toggle.*  
  `C++` · Лицензия: GPL-3.0

---

## Клиенты / Desktop & Console Clients

- **[curlysasha/MeshRadar](https://github.com/curlysasha/MeshRadar)** — Современный десктопный клиент для управления Meshtastic-сетью. Поддерживает подключение по Serial, TCP и BLE; чат с подтверждениями доставки; список нод с телеметрией (батарея, SNR, координаты); интерактивная карта сети; traceroute с визуализацией маршрутов; история сообщений в SQLite; WebSocket для обновлений в реальном времени; RU/EN интерфейс. Распространяется как portable EXE для Windows и Docker-образ.  
  *Modern Meshtastic desktop client. Serial/TCP/BLE connection, chat with delivery confirmation, node list with telemetry, interactive network map, traceroute visualisation, SQLite history, real-time WebSocket, RU/EN UI. Portable Windows EXE and Docker available.*  
  `Python` / `TypeScript` (React) · Лицензия: GPLv3 + Commons Clause

- **[peerat/meshTools → meshTalk](https://github.com/peerat/meshTools)** — Исследовательский десктопный P2P-клиент для Meshtastic с GUI (PySide6). Реализует best-effort обмен данными с ACK/повторами, трассировку маршрутов (traceroute), обмен ключами X25519/HKDF, транспортный контейнер AES-256-GCM, адаптивное сжатие (DEFLATE/ZLIB/BZ2/LZMA/ZSTD), статусы доставки и runtime-наблюдаемость.  
  *Experimental Meshtastic P2P desktop GUI (PySide6) with best-effort ACK/retry delivery, traceroute, X25519/HKDF key exchange, AES-256-GCM transport, adaptive ZSTD compression, delivery status tracking.*  
  `Python` · Лицензия: Apache-2.0

- **[skobkin/meshgo](https://git.skobk.in/skobkin/meshgo)** ([зеркало GitHub](https://github.com/skobkin/meshgo)) — Десктопный клиент для Meshtastic под Windows и Linux, написанный на Go. Поддерживает IP (WiFi) и Serial (USB) транспорт; чат, список нод, traceroute, карту на основе OpenStreetMap, редактирование настроек устройства и каналов. Релизы для Windows/Linux доступны на Forgejo.  
  *Desktop Meshtastic client for Windows and Linux written in Go. IP and Serial transport, chat, node list, traceroute, OSM map, device/channel settings editor. Binaries available via Forgejo releases.*  
  `Go` · Лицензия: MIT

- **[covox/meshapp](https://git.privatepractice.app/covox/meshapp)** — Десктопный клиент для Meshtastic от [@coVox](https://t.me/coVox).  
  *Desktop Meshtastic client by [@coVox](https://t.me/coVox).*

- **[mrSatang/meshtastic_monkey](https://github.com/mrSatang/meshtastic_monkey)** — Интерактивный терминальный (CLI) клиент для Meshtastic на Linux/SSH. Позволяет отправлять и получать сообщения через mesh-сеть прямо из терминала; поддерживает публичные и приватные сообщения, автодополнение имён нод по Tab, историю ввода, отслеживание ACK, автоответ на `ping`/`test`, отображение RSSI/SNR/хопов. Идеален для удалённого управления нодой через SSH.  
  *Interactive terminal (CLI) Meshtastic client for Linux/SSH. Public and private messages, node name autocomplete, input history, ACK tracking, ping auto-reply, RSSI/SNR/hop display. Ideal for remote node management over SSH.*  
  `Python`

---

## Инструменты / Tools

- **[playmean/mtsh](https://github.com/playmean/mtsh)** — Удалённая оболочка (remote shell) через Meshtastic. Позволяет выполнять shell-команды на удалённом узле через текстовые сообщения mesh-сети. Поддерживает подключение через serial, BLE и HTTP; chunked-передача больших ответов с подтверждениями и повторными попытками, адаптивное сжатие, белые списки узлов. Включает режим копирования файлов (`cp`) и прямой отправки сообщений (`msg`).  
  *Remote shell over Meshtastic text messages. Run shell commands on a remote node via the mesh. Supports serial/BLE/HTTP, chunked output with ACKs and retries, adaptive compression, node whitelisting. Also supports file copy (`cp`) and plain message send (`msg`) modes.*  
  `Go` · Лицензия: MIT

- **[skrashevich/go-meshtastic-serial2tcp](https://github.com/skrashevich/go-meshtastic-serial2tcp)** — TCP ↔ Serial мост для устройств Meshtastic. Слушает на TCP-порту и пересылает фреймы Meshtastic на серийный порт. Поддерживает несколько одновременных клиентов, режим read-only для вторичных клиентов, mDNS-обнаружение, Docker-образ.  
  *Small TCP ↔ serial bridge for Meshtastic devices. Multiple concurrent TCP clients, read-only mode for secondary clients, mDNS discovery, Docker image available.*  
  `Go` · Лицензия: GPL-3.0

- **[mrekin/MeshtasticCustomBoards](https://github.com/mrekin/MeshtasticCustomBoards)** + **[веб-флэшер](https://mrekin.duckdns.org/flasher)** — Веб-установщик (флэшер) кастомных прошивок Meshtastic с русским интерфейсом. Содержит профили нестандартных плат (DIY-устройства на ESP32/NRF52/RP2040) для сборочной системы Meshtastic. Через веб-флэшер доступны прошивки с поддержкой русского языка для OLED-дисплеев, русифицированные прошивки с улучшенным энергосберегающим режимом (ветка m1nl), а также прошивки для MeshCore.  
  *Web flasher for custom Meshtastic firmware with Russian UI. Contains custom board profiles for DIY devices (ESP32/NRF52/RP2040). Offers Russian-language display firmware, energy-saving variants, and MeshCore builds.*  
  `YAML` / `Gerber`

- **[peerat/meshTools](https://github.com/peerat/meshTools)** — Набор Python-утилит для исследования Meshtastic-сетей: `meshLogger` — сбор трассировок и событий, логирование в файлы и SQLite; `graphGen` — построение графов mesh-сети (Graphviz / D3.js); `meshTalk` — P2P-клиент с ACK/повторами; `nodeDbUpdater` — обновление базы нод.  
  *Collection of Python tools for Meshtastic mesh research: meshLogger (traceroute/event logging to files + SQLite), graphGen (Graphviz/D3 mesh graph generation), meshTalk (P2P client with ACK/retry), nodeDbUpdater.*  
  `Python` · Лицензия: Apache-2.0

- **Кодирование кириллицы гомоглифами** — Вклад [@luigivampa92](https://t.me/luigivampa92) в официальное Android-приложение Meshtastic: кодирование части кирилличных букв латинскими гомоглифами для уменьшения размера пакета. Опция «Компактное кодирование для Кириллицы» появилась в официальном приложении начиная с версии 2.7.13 (раздел «Приложение» → настройки).  
  *Contribution by [@luigivampa92](https://t.me/luigivampa92) to the official Meshtastic Android app: encoding Cyrillic characters using Latin homoglyphs to reduce packet size. Available as "Compact Cyrillic Encoding" toggle since app v2.7.13.*

---

## Инфраструктура / Infrastructure

- **[capricornusx/meshtastic-mqtt-exporter](https://github.com/capricornusx/meshtastic-mqtt-exporter)** — Экспорт телеметрии Meshtastic-устройств в Prometheus. Встроенный MQTT-брокер на базе mochi-mqtt, поддержка TLS/QoS/Retention, метрики: батарея, температура, влажность, давление, RSSI, SNR; интеграция с AlertManager для отправки алертов в LoRa mesh-сеть; персистентность метрик между перезапусками (JSON, каждые 5 минут).  
  *Export Meshtastic device telemetry to Prometheus. Built-in mochi-mqtt broker, TLS/QoS/Retention support, battery/temp/humidity/pressure/RSSI/SNR metrics, AlertManager integration to push alerts into the LoRa mesh, persistent metrics across restarts.*  
  `Go` · Лицензия: MIT

- **[54ph3r/meshtastic-network-monitor](https://hub.docker.com/r/54ph3r/meshtastic-network-monitor)** — Docker-контейнер, который транслирует сообщения из Meshtastic-сети в Telegram-канал/группу через бота. Веб-интерфейс для просмотра сообщений и нод. Настраивается через переменные окружения: выбор каналов, уведомления о новых/изменённых нодах, ежедневные отчёты по метрикам загрузки, активности, моделям устройств и координатам.  
  *Docker container that bridges Meshtastic mesh messages into a Telegram channel/group via bot. Web UI for message/node monitoring. Configurable via env vars: channel selection, new/changed node notifications, daily load/activity/hardware/position reports.*  
  `Python` (Docker)

---

## Карты / Maps

- **[ONEmesh — map.onemesh.ru](https://map.onemesh.ru/)** — Карта устройств Meshtastic в России с разбивкой по городам. Собственный улучшенный MQTT-сервер с тремя режимами работы (only uplink / downlink zero-hop / downlink без ограничений), отслеживанием нод с downlink и раздельными слоями для них, контролем данных от недобросовестных пользователей. Подключившись к MQTT-серверу ONEmesh, нода автоматически появляется и на других картах (meshmap, liamcottle, taubetele). Также предоставляет Telegram-бота для трансляции сообщений из mesh-сети в Telegram. Телеграм-группа: [@onemesh_ru](https://t.me/onemesh_ru).  
  *Map of Meshtastic nodes across Russia by city. Custom MQTT server with three operation modes, downlink node tracking, abuse control. Connecting to ONEmesh MQTT also propagates your node to meshmap, liamcottle, and taubetele maps. Includes a Telegram bot bridging mesh messages into Telegram.*

---

## Сборщики / Build Tools

- **[skrashevich/meshtastic-firmware-builder](https://github.com/skrashevich/meshtastic-firmware-builder)** — Веб-приложение для сборки прошивки Meshtastic из неофициальных форк-репозиториев. Пользователь указывает URL репозитория, выбирает ветку/тег и устройство — бэкенд клонирует репозиторий и запускает `pio run` в Docker-контейнере с PlatformIO. Фронтенд отображает live-логи сборки и ссылки на скачивание файлов прошивки. Поддержка RU/EN, CAPTCHA, очередь сборок, all-in-one Docker-образ.  
  *Web application for building Meshtastic firmware from any fork repository. Provide a repo URL, pick a branch/tag and target device, get firmware binaries. Go backend, React/TypeScript frontend, PlatformIO builder in Docker, live build logs, RU/EN UI, CAPTCHA, build queue.*  
  `Go` / `TypeScript`

---

## Сообщество / Community

- **[Telegram: meshtastic_russia](https://t.me/meshtastic_russia)** — Основной русскоязычный Telegram-чат сообщества Meshtastic (~9 500 участников).  
  *Main Russian-speaking Meshtastic community Telegram group (~9 500 members).*

---

## Вклад / Contributing

Хотите добавить проект? Откройте Pull Request или Issue. Принимаются проекты, связанные с Meshtastic, от русскоязычных / CIS разработчиков.

*Want to add a project? Open a Pull Request or Issue. Projects related to Meshtastic from Russian-speaking / CIS developers are welcome.*

---

## Лицензия / License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

Содержимое этого списка находится в общественном достоянии (CC0).  
*This list is released into the public domain (CC0).*
