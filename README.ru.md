<p align="center"><b>PUBLIC PROJECT · ПУБЛИЧНЫЙ ПРОЕКТ</b><br>
<a href="https://github.com/svllvsxprod/photonicat-companion">Original repository / Оригинальный репозиторий ↗</a> · <a href="https://github.com/svllvsx">Portfolio / Портфолио</a></p>

> **Android and desktop router companion.** Помощник для роутера на Android и компьютере.
> This is a README showcase. Source code, releases and development instructions belong to the original repository.
> Это README-витрина. Исходники, релизы и команды разработки относятся к оригинальному репозиторию.

---

<p align="center"><a href="README.md">English</a> · <a href="README.ru.md">Русский</a></p>
<h1 align="center">Photonicat Companion</h1>
<p align="center">Мониторинг роутера, управление устройством и VPN с Android, macOS и Windows.</p>
<p align="center"><img alt="Flutter" src="https://img.shields.io/badge/Flutter-f4e600?style=flat-square"> <img alt="Python" src="https://img.shields.io/badge/Python-f4e600?style=flat-square"> <img alt="Bluetooth LE" src="https://img.shields.io/badge/Bluetooth%20LE-f4e600?style=flat-square"></p>

<p align="center">
<img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/current-status.png" width="30%" alt="Status demo">
<img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/current-vpn.png" width="30%" alt="Current Direct / VPN controls">
<img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/current-controls.png" width="30%" alt="Current screen and fan controls">
</p>
> Иллюстрации Android-версии до настольного выпуска: виджеты отрисованы 21.10.2026 в изолированном демо-окружении. Показатели, имена и адреса вымышлены; брендинг заменён. Это не замер работающего устройства.

## Версия 0.7.5 beta

[**Скачать APK, DMG для Mac и EXE для Windows**](https://github.com/svllvsxprod/photonicat-companion/releases/tag/v0.7.5-beta.1) · [Мастер настройки со скриншотами](https://github.com/svllvsxprod/photonicat-companion/blob/main/docs/public/SETUP_RU.md) · [Установка и повседневное управление](https://github.com/svllvsxprod/photonicat-companion/blob/main/docs/public/USAGE_RU.md)

Приложение на компьютере восстанавливает связь при переходе **Wi-Fi ↔ Ethernet**. Поиск учитывает шлюзы всех активных адаптеров и проверяет сохранённый ключ роутера. Команды, прерванные обрывом, автоматически не повторяются.

| Возможность | Реализация |
| --- | --- |
| Android 12+ | Управление по Bluetooth LE с защищённой привязкой; APK в релизе. |
| macOS 12+, Apple Silicon | Панель из строки меню, связь по локальной сети; автозапуск по выбору с macOS 13. |
| Windows x64 | Панель из трея с учётом экрана, автозапуск по выбору, установщик и portable ZIP. |
| Первая настройка | Компьютерный мастер обнаруживает оборудование, устанавливает службу и получает ключ роутера. |
| VPN | Подписки Mihomo, профили AmneziaWG, один выбранный профиль на каждом ядре, режимы Direct/VPN. |
| Пять разделов | Состояние, устройства, VPN, роутер и входящие СМС. |
| Управление | Wi-Fi, яркость и таймер экрана, вентилятор; батарея, CPU, RAM и трафик. |

GearUP из приложения удалён. Мастер не прошивает модем и не устанавливает неизвестные драйверы.

## С чего начать

1. Подключите компьютер к клиентской сети Photonicat по Wi-Fi или Ethernet.
2. Установите приложение, откройте значок кота и нажмите **«Настроить роутер»**. Понадобятся локальный адрес роутера и административный пароль SSH.
3. Пройдите [мастер со скриншотами](https://github.com/svllvsxprod/photonicat-companion/blob/main/docs/public/SETUP_RU.md) и сохраните ключ привязки в менеджере паролей.
4. На Android установите APK, включите Bluetooth, вставьте этот ключ и разрешите доступ к устройствам поблизости. Телефон управляет по BLE; первичная установка службы выполняется с компьютера.
5. Добавьте собственную VPN-подписку/конфигурацию и выберите Direct или VPN для нужного клиентского подключения.

Ключей владельца, личных подписок и конфигурации действующего роутера в выпуске нет. Обновление совместимой сборки устанавливается поверх прежней; перед удалением приложения сохраните ключ.

## Исходники и сборка

[Исходники и команды сборки](https://github.com/svllvsxprod/photonicat-companion).

## Что проверено и что ещё нет

Для настольной версии прошли анализ и 39 Flutter-тестов на Mac и Windows. Реальная связь с роутером восстановилась после имитации потери адаптера без изменения сети ОС. Физическое переключение Wi-Fi/кабеля в этом выпуске не выполнялось. В Windows-среде прошли установка, скрытый запуск и удаление; это не заменяет проверку настоящего ПК с роутером. APK собран, подпись проверена; запуск именно нового APK на телефоне при подготовке релиза не проверен.

Мастер рассчитан на Photonicat 2 с PhotonicatWrt 26.04.1; полный путь на заводском устройстве пока не подтверждён. iOS включён в исходники, но проверенного выпуска нет. Протокол не проходил независимый аудит. EXE пока без подписи, Mac — с подписью разработки Apple без нотариализации, APK — с текущим тестовым сертификатом. [Подробности выпуска](https://github.com/svllvsxprod/photonicat-companion/blob/main/docs/public/RELEASE_0_7_5.md).

## Права и зависимости

Исходники опубликованы для ознакомления. Общая лицензия на повторное использование собственного кода не выбрана. Сторонние компоненты сохраняют свои условия: [RIGHTS.md](https://github.com/svllvsxprod/photonicat-companion/blob/main/RIGHTS.md). К выпуску приложены соответствующие исходники Mihomo/AmneziaWG и лицензии. Это независимый проект, не продукт производителя роутера.

---

<p align="center">
<a href="https://t.me/tribute/app?startapp=dK9j"><img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/support-tribute.svg" height="36" alt="Support via Tribute"></a>
<a href="https://nowpayments.io/donation/svllvsx"><img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/support-nowpayments.svg" height="36" alt="Support via NOWPayments"></a>
<a href="https://t.me/svllvsxprod"><img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/telegram.svg" height="36" alt="Telegram"></a>
</p>
