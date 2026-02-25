# Awesome Meshtastic RU [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Кураторский список проектов, связанных с [Meshtastic](https://meshtastic.org), от русскоязычных разработчиков.  
> A curated list of [Meshtastic](https://meshtastic.org)-related projects from Russian-speaking / CIS developers.

[Meshtastic](https://meshtastic.org) — это проект с открытым исходным кодом, позволяющий использовать недорогие LoRa-устройства для создания децентрализованных mesh-сетей с шифрованием.

---

## Содержание / Contents

- [Прошивки / Firmware](#прошивки--firmware)
- [UI-библиотеки / UI Libraries](#ui-библиотеки--ui-libraries)
- [Инструменты / Tools](#инструменты--tools)
- [Инфраструктура / Infrastructure](#инфраструктура--infrastructure)
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

## Инструменты / Tools

- **[playmean/mtsh](https://github.com/playmean/mtsh)** — Удалённая оболочка (remote shell) через Meshtastic. Позволяет выполнять shell-команды на удалённом узле через текстовые сообщения mesh-сети. Поддерживает подключение через serial, BLE и HTTP; chunked-передача больших ответов с подтверждениями и повторными попытками, адаптивное сжатие, белые списки узлов. Включает режим копирования файлов (`cp`) и прямой отправки сообщений (`msg`).  
  *Remote shell over Meshtastic text messages. Run shell commands on a remote node via the mesh. Supports serial/BLE/HTTP, chunked output with ACKs and retries, adaptive compression, node whitelisting. Also supports file copy (`cp`) and plain message send (`msg`) modes.*  
  `Go` · Лицензия: MIT

- **[skrashevich/go-meshtastic-serial2tcp](https://github.com/skrashevich/go-meshtastic-serial2tcp)** — TCP ↔ Serial мост для устройств Meshtastic. Слушает на TCP-порту и пересылает фреймы Meshtastic на серийный порт. Поддерживает несколько одновременных клиентов, режим read-only для вторичных клиентов, mDNS-обнаружение, Docker-образ.  
  *Small TCP ↔ serial bridge for Meshtastic devices. Multiple concurrent TCP clients, read-only mode for secondary clients, mDNS discovery, Docker image available.*  
  `Go` · Лицензия: GPL-3.0

---

## Инфраструктура / Infrastructure

- **[capricornusx/meshtastic-mqtt-exporter](https://github.com/capricornusx/meshtastic-mqtt-exporter)** — Экспорт телеметрии Meshtastic-устройств в Prometheus. Встроенный MQTT-брокер на базе mochi-mqtt, поддержка TLS/QoS/Retention, метрики: батарея, температура, влажность, давление, RSSI, SNR; интеграция с AlertManager для отправки алертов в LoRa mesh-сеть; персистентность метрик между перезапусками (JSON, каждые 5 минут).  
  *Export Meshtastic device telemetry to Prometheus. Built-in mochi-mqtt broker, TLS/QoS/Retention support, battery/temp/humidity/pressure/RSSI/SNR metrics, AlertManager integration to push alerts into the LoRa mesh, persistent metrics across restarts.*  
  `Go` · Лицензия: MIT

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
