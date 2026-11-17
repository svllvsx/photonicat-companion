<p align="center"><b>PUBLIC PROJECT · ПУБЛИЧНЫЙ ПРОЕКТ</b><br>
<a href="https://github.com/svllvsxprod/photonicat-companion">Original repository / Оригинальный репозиторий ↗</a> · <a href="https://github.com/svllvsx">Portfolio / Портфолио</a></p>

> **Android and desktop router companion.** Помощник для роутера на Android и компьютере.
> This is a README showcase. Source code, releases and development instructions belong to the original repository.
> Это README-витрина. Исходники, релизы и команды разработки относятся к оригинальному репозиторию.

---

<p align="center"><a href="README.md">English</a> · <a href="README.ru.md">Русский</a></p>
<h1 align="center">Photonicat Companion</h1>
<p align="center">Router telemetry, VPN and device controls on Android, macOS and Windows.</p>
<p align="center"><img alt="Flutter" src="https://img.shields.io/badge/Flutter-f4e600?style=flat-square"> <img alt="Python" src="https://img.shields.io/badge/Python-f4e600?style=flat-square"> <img alt="Bluetooth LE" src="https://img.shields.io/badge/Bluetooth%20LE-f4e600?style=flat-square"></p>

<p align="center">
<img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/current-status.png" width="30%" alt="Status demo">
<img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/current-vpn.png" width="30%" alt="Current Direct / VPN controls">
<img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/current-controls.png" width="30%" alt="Current screen and fan controls">
</p>
> Illustrations from the 2026-10-21 Android demo, preceding the desktop release; widgets rendered in an isolated demo environment. Readings, names and addresses are fictional; branding is replaced. This is not a live-device measurement.

## Version 0.7.5 beta

[**Download APK, Mac DMG and Windows EXE**](https://github.com/svllvsxprod/photonicat-companion/releases/tag/v0.7.5-beta.1) · [Setup guide with screenshots (RU)](https://github.com/svllvsxprod/photonicat-companion/blob/main/docs/public/SETUP_RU.md) · [Installation and everyday use (RU)](https://github.com/svllvsxprod/photonicat-companion/blob/main/docs/public/USAGE_RU.md)

Desktop connections now recover when switching **Wi-Fi ↔ Ethernet**. Discovery checks gateways on all active adapters and verifies the saved router key before accepting a connection. Lost commands are not automatically replayed.

| Feature | What is included |
| --- | --- |
| Android 12+ | Bluetooth LE control with protected pairing; APK in the release. |
| macOS 12+, Apple Silicon | Menu-bar panel, local-network control, optional login startup on macOS 13+. |
| Windows x64 | Tray panel with display-aware positioning, optional startup, installer and portable ZIP. |
| First setup | Desktop wizard detects supported hardware, installs the companion service and retrieves the router key. |
| VPN | Mihomo subscriptions and AmneziaWG profiles; one selected profile per core; Direct/VPN routing controls. |
| Five tabs | Status, devices, VPN, router controls and incoming SMS. |
| Router controls | Wi-Fi, screen brightness/timeout, fan modes; battery, CPU, RAM and traffic readings. |

GearUP is no longer exposed in the app. The installer does not flash modem firmware or install unknown drivers.

## Get started

1. Connect your computer to the Photonicat client network over Wi-Fi or Ethernet.
2. Install the desktop app, open its cat icon and choose **«Настроить роутер»**. You need the router's local address and administrator SSH password.
3. Follow the [illustrated wizard](https://github.com/svllvsxprod/photonicat-companion/blob/main/docs/public/SETUP_RU.md), then save the generated/retrieved pairing key in a password manager.
4. On Android, install the APK, enable Bluetooth, enter this key and allow Nearby devices access. Android controls the router over BLE; it does not run the first-install wizard.
5. Add your own VPN subscription/configuration and choose Direct or VPN for the desired client interface.

No owner key, subscription or live router configuration is shipped. Existing users can update over their compatible installation; preserve their pairing key before uninstalling.

## Source and build

[Source code and build instructions](https://github.com/svllvsxprod/photonicat-companion).

## Verification and limits

The 0.7.5 desktop code passed 39 Flutter tests and analysis on Mac and Windows. An authenticated live-router test resumed status updates after simulated adapter loss without changing OS networking. Physical Wi-Fi/cable switching was not performed for this release. Windows installation, hidden startup and uninstall passed in CI; this is not a substitute for a physical-PC/router test. APK build/signature verification passed; this new APK has not been launched on a phone during release preparation.

The first-install wizard targets Photonicat 2 with PhotonicatWrt 26.04.1; a full factory-fresh installation remains unverified. iOS is a source target, not a tested release. The protocol has not received an independent security audit. Windows EXE is unsigned; Mac uses an Apple development signature without notarization; APK uses the current test certificate. See [release notes](https://github.com/svllvsxprod/photonicat-companion/blob/main/docs/public/RELEASE_0_7_5.md).

## Rights and dependencies

Sources are published for inspection. No general reuse license has been selected for original project code. Third-party components retain their own terms: [RIGHTS.md](https://github.com/svllvsxprod/photonicat-companion/blob/main/RIGHTS.md). Matching Mihomo/AmneziaWG sources and licenses accompany the release. This is an independent project, not a manufacturer product.

---

<p align="center">
<a href="https://t.me/tribute/app?startapp=dK9j"><img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/support-tribute.svg" height="36" alt="Support via Tribute"></a>
<a href="https://nowpayments.io/donation/svllvsx"><img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/support-nowpayments.svg" height="36" alt="Support via NOWPayments"></a>
<a href="https://t.me/svllvsxprod"><img src="https://raw.githubusercontent.com/svllvsxprod/photonicat-companion/main/docs/readme/telegram.svg" height="36" alt="Telegram"></a>
</p>
