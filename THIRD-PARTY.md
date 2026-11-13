# Сторонние компоненты Dissordium

**Dissordium 1.0.0 Beta**

Лицензия оригинального клиента не заменяет лицензии стороннего программного обеспечения и графики. Ниже указан состав актуального установщика. Полные тексты и авторские уведомления находятся в установленной папке `licenses`; эта таблица их не заменяет.

| Компонент | Версия | Автор / проект | Лицензия и материалы в поставке | Источник |
|---|---|---|---|---|
| Zapret / winws | 72.13 | bol-van и участники | MIT; `LICENSE-zapret.txt` | [Zapret](https://github.com/bol-van/zapret) |
| WinDivert | 2.2.2-A x64 | Basil Projects и участники | LGPL-3.0; точные условия в `LICENSE-windivert.txt` и `GPL-3.txt` | [WinDivert](https://github.com/basil00/WinDivert) |
| Cygwin DLL | 3.4.10 | Cygwin и правообладатели отдельных частей | LGPL-3.0-or-later с дополнительными разрешениями; уведомления newlib и полные условия в `Cygwin-*.txt` | [Cygwin](https://cygwin.com/licensing.html) |
| sing-box | 1.12.12 | SagerNet и участники | GPL-3.0-or-later; `LICENSE-sing-box.txt` | [sing-box](https://github.com/SagerNet/sing-box) |
| Xray-core | 26.11.9 | XTLS и участники | MPL-2.0; `Xray-MPL-2.0.txt` | [Xray-core](https://github.com/XTLS/Xray-core) |
| Wintun, официальный бинарник AMD64 | 0.14.1 | WireGuard LLC | Собственные условия Prebuilt Binaries License; `LICENSE-wintun.txt`. Лицензию исходного проекта нельзя автоматически приписывать готовой DLL | [Wintun](https://www.wintun.net/) |
| Microsoft .NET / WPF | 10.0.14 | Microsoft и участники | MIT и уведомления отдельных компонентов; `LICENSE-dotnet.txt`, `NOTICES-dotnet.txt`, `NOTICES-runtime.txt`, `NOTICES-windowsdesktop.txt` | [.NET](https://github.com/dotnet/runtime), [WPF](https://github.com/dotnet/wpf) |
| YamlDotNet | 16.3.0 | Antoine Aubry и участники | MIT; `YamlDotNet-MIT.txt` | [YamlDotNet](https://github.com/aaubry/YamlDotNet) |
| Inno Setup, компоненты установщика | 6.4.3 | Jordan Russell, Martijn Laan и другие правообладатели | Собственная лицензия и дополнительные уведомления; `LICENSE-InnoSetup.txt` | [Inno Setup](https://jrsoftware.org/isinfo.php) |
| Simple Icons, используемые иконки сервисов | 11.15.0 | Участники Simple Icons | CC0-1.0; `Simple-Icons-CC0.md`. Названия и товарные знаки сохраняют своих правообладателей | [Simple Icons](https://github.com/simple-icons/simple-icons) |
| Twemoji, неизменённые изображения флагов и emoji | 14.0.2 | Twitter, Inc. и участники | CC-BY-4.0; `Twemoji-LICENSE-GRAPHICS.txt` | [Исходный набор Twemoji](https://github.com/twitter/twemoji/tree/v14.0.2/assets/72x72) |

Для LGPL-3.0 в таблице используется обозначение версии лицензии; окончательные права определяются включёнными полными текстами и уведомлениями. Для собственных условий Wintun и Inno Setup универсальный SPDX-идентификатор здесь не заявляется.

## Встроенные зависимости

sing-box и Xray содержат зависимости Go с отдельными лицензиями. В поставке сохранены:

- `licenses/sing-box-modules.txt`: точные версии и h1-хеши 93 модулей sing-box;
- `licenses/xray-modules.txt`: точные версии и h1-хеши 44 модулей Xray;
- `licenses/go-notices/`: тексты лицензий и уведомления соответствующих модулей;
- `licenses/Go-LICENSE.txt`: лицензия компонентов Go.

Номера версий модулей определяются этими перечнями конкретного выпуска; им нельзя приписывать единую лицензию сетевого ядра. Уведомления платформы .NET также охватывают её сторонние компоненты. Фирменный логотип и изображения Dissordium не предоставляются как часть лицензий Simple Icons или Twemoji.

## Исходные материалы и распространение

К текущему Draft Release приложен `THIRD_PARTY_SOURCES.zip`: соответствующие исходники Zapret, WinDivert, Cygwin, sing-box и Xray, архивы их модулей Go, лицензионные материалы и инструкции сборки в исходных деревьях. Проприетарный исходный код клиента Dissordium в этот архив не входит.

Вложения текущего [GitHub Draft](https://github.com/shazam808/dissordium-releases/releases): установщик, `THIRD_PARTY_SOURCES.zip` и `SHA256SUMS.txt`. Файл контрольных сумм содержит SHA-256 установщика и архива; порядок проверки описан в [инструкции установки](INSTALLATION.md#проверка-контрольных-сумм). Репозиторий остаётся приватным, релиз — Draft + Pre-release. Скачать вложения могут только пользователи с необходимым доступом; публичная загрузка пока недоступна.

При публичном распространении архив соответствующих исходных материалов и лицензионные уведомления должны оставаться доступными вместе с выпуском. Владелец должен проверить полноту комплекта и выбранный способ предоставления материалов по применимым лицензиям. Добавление вложений не означает публикацию релиза.

Сетевые ядра запускаются отдельными процессами; отдельно поставляемые LGPL-библиотеки остаются заменяемыми. Права получателей и предусмотренные LGPL исключения сохранены в действующей [лицензии клиента](LICENSE.txt). Контрольная сумма проверяет целостность, а не подлинность издателя. Юридическая проверка условий распространения перед публичным выпуском остаётся отдельной задачей.
