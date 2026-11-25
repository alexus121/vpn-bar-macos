# VPN Bar

**Русский:** Небольшое приложение для macOS, которое управляет системными VPN-подключениями прямо из строки меню. Левый клик переключает последний выбранный VPN; правый клик открывает список подключений.

**English:** A small macOS menu bar app for controlling built-in VPN profiles. Left-click toggles the last selected VPN; right-click opens the connection list.

![VPN Bar quick toggle preview](quick-toggle.svg)

![VPN Bar profile and icon picker preview](profile-picker.svg)

*Visual previews of the app interface / Векторные превью интерфейса приложения.*

## Русский

### Что это

VPN Bar позволяет быстро включать и выключать VPN-профили macOS, не открывая Системные настройки. Если подключений несколько, можно выбрать нужное из панели приложения. Цвет обычного значка при подключении подстраивается под акцентный цвет macOS; обезьянка сохраняет свои исходные варианты оформления.

### Как пользоваться

1. Установите приложение из `dist/VPN Bar Installer.pkg` или распакуйте `dist/VPN Bar.app.zip` в папку «Программы».
2. Добавьте VPN-профиль в **Системные настройки → VPN**. Приложение видит системные профили macOS.
3. Запустите VPN Bar. **Левый клик** по значку в строке меню включает или выключает последний выбранный VPN; если VPN уже подключён, клик переключает активное подключение.
4. **Правый клик** по значку открывает панель со списком VPN. Выберите другой профиль, чтобы подключиться к нему.
5. Чтобы сменить значок, нажмите правой кнопкой на карточку подключения в панели и выберите **«Сменить значок»**. В сетке выбора значков показаны только изображения, без подписей.

### Совместимость и примечания

- macOS 13 или новее; сборка содержит версии для Apple silicon и Intel.
- Поддерживаются профили, отображаемые командой `scutil --nc list`. VPN-клиенты, которые работают только внутри собственного приложения и не добавляют системный профиль macOS, не отображаются.
- VPN Bar не хранит пароли: подключением управляет macOS с использованием сохранённых системных данных.
- Эта тестовая сборка не подписана сертификатом Developer ID и не нотариализована Apple. При первом запуске macOS может показать предупреждение безопасности.

## English

### What it is

VPN Bar lets you quickly turn macOS VPN profiles on or off without opening System Settings. When you have multiple profiles, choose one from the app panel. The connected color of regular icons follows the macOS accent color; the monkey keeps its original artwork and colors.

### How to use it

1. Install `dist/VPN Bar Installer.pkg`, or unzip `dist/VPN Bar.app.zip` and move the app to Applications.
2. Add a VPN profile in **System Settings → VPN**. VPN Bar works with profiles managed by macOS.
3. Open VPN Bar. **Left-click** its menu bar icon to toggle the last selected VPN; if a VPN is already connected, the click toggles the active connection.
4. **Right-click** the menu bar icon to open the VPN list. Choose another profile to connect to it.
5. To change the menu bar icon, right-click the connection card in the panel and choose **“Change Icon.”** The icon grid has no captions.

### Compatibility and notes

- macOS 13 or later; the build includes Apple silicon and Intel versions.
- VPN Bar detects profiles listed by `scutil --nc list`. VPN clients that only manage tunnels inside their own app and do not create a macOS system profile are not listed.
- VPN Bar does not store passwords. macOS manages the connection and uses credentials saved in the system.
- This test build is not signed with a Developer ID certificate or notarized by Apple. macOS may show a security warning on first launch.
