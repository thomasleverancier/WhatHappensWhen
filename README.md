Этот репозиторий представляет собой попытку ответить на вечный вопрос собеседования: "Что происходит, когда вы вводите google.com в адресную строку браузера и нажимаете Enter?"

Но вместо обычного рассказа мы попытаемся ответить на этот вопрос максимально подробно. Никаких пропусков.

Все это лицензировано в соответствии с условиями лицензии Creative Commons Zero.

Перевод [статьи](https://github.com/alex/what-happens-when) с помощью ИИ.

## Содержание

- [Нажатие клавиши "g"](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%BD%D0%B0%D0%B6%D0%B0%D1%82%D0%B8%D0%B5-%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D1%88%D0%B8-g)
- [Клавиша "enter" нажимается до упора](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D1%88%D0%B0-enter-%D0%BD%D0%B0%D0%B6%D0%B8%D0%BC%D0%B0%D0%B5%D1%82%D1%81%D1%8F-%D0%B4%D0%BE-%D1%83%D0%BF%D0%BE%D1%80%D0%B0)
- [Срабатывает прерывание [НЕ для USB-клавиатур]](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D1%81%D1%80%D0%B0%D0%B1%D0%B0%D1%82%D1%8B%D0%B2%D0%B0%D0%B5%D1%82-%D0%BF%D1%80%D0%B5%D1%80%D1%8B%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BD%D0%B5-%D0%B4%D0%BB%D1%8F-usb-%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80)
- [(В Windows) Приложению отправляется сообщение WM_KEYDOWN](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D1%81%D1%80%D0%B0%D0%B1%D0%B0%D1%82%D1%8B%D0%B2%D0%B0%D0%B5%D1%82-%D0%BF%D1%80%D0%B5%D1%80%D1%8B%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BD%D0%B5-%D0%B4%D0%BB%D1%8F-usb-%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80)
- [(В OS X) Приложению отправляется NSEvent KeyDown](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%B2-os-x-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8E-%D0%BE%D1%82%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D1%8F%D0%B5%D1%82%D1%81%D1%8F-nsevent-keydown)
- [(В GNU/Linux) Xorg сервер прослушивает коды клавиш](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%B2-gnulinux-xorg-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80-%D0%BF%D1%80%D0%BE%D1%81%D0%BB%D1%83%D1%88%D0%B8%D0%B2%D0%B0%D0%B5%D1%82-%D0%BA%D0%BE%D0%B4%D1%8B-%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D1%88)
- [Разбор URL](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D1%80%D0%B0%D0%B7%D0%B1%D0%BE%D1%80-url)
- [Это URL или поисковый запрос?](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D1%8D%D1%82%D0%BE-url-%D0%B8%D0%BB%D0%B8-%D0%BF%D0%BE%D0%B8%D1%81%D0%BA%D0%BE%D0%B2%D1%8B%D0%B9-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81)
- [Преобразование не-ASCII символов Unicode в имени хоста](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%BF%D1%80%D0%B5%D0%BE%D0%B1%D1%80%D0%B0%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BD%D0%B5-ascii-%D1%81%D0%B8%D0%BC%D0%B2%D0%BE%D0%BB%D0%BE%D0%B2-unicode-%D0%B2-%D0%B8%D0%BC%D0%B5%D0%BD%D0%B8-%D1%85%D0%BE%D1%81%D1%82%D0%B0)
- [Проверка списка HSTS](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0-%D1%81%D0%BF%D0%B8%D1%81%D0%BA%D0%B0-hsts)
- [DNS-запрос](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#dns-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81)
- [Процесс ARP](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%BF%D1%80%D0%BE%D1%86%D0%B5%D1%81%D1%81-arp)
- [Открытие сокета](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%BE%D1%82%D0%BA%D1%80%D1%8B%D1%82%D0%B8%D0%B5-%D1%81%D0%BE%D0%BA%D0%B5%D1%82%D0%B0)
- [TLS рукопожатие](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#tls-%D1%80%D1%83%D0%BA%D0%BE%D0%BF%D0%BE%D0%B6%D0%B0%D1%82%D0%B8%D0%B5)
- [Если пакет потерян](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%B5%D1%81%D0%BB%D0%B8-%D0%BF%D0%B0%D0%BA%D0%B5%D1%82-%D0%BF%D0%BE%D1%82%D0%B5%D1%80%D1%8F%D0%BD)
- [HTTP протокол](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#http-%D0%BF%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB)
- [Обработка HTTP-запроса сервером](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%BE%D0%B1%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0-http-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%B0-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%BE%D0%BC)
- [За кулисами браузера](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%B7%D0%B0-%D0%BA%D1%83%D0%BB%D0%B8%D1%81%D0%B0%D0%BC%D0%B8-%D0%B1%D1%80%D0%B0%D1%83%D0%B7%D0%B5%D1%80%D0%B0)
- [Браузер](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%B1%D1%80%D0%B0%D1%83%D0%B7%D0%B5%D1%80)
- [HTML парсинг](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#html-%D0%BF%D0%B0%D1%80%D1%81%D0%B8%D0%BD%D0%B3)
- [CSS интерпретация](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#css-%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D0%BF%D1%80%D0%B5%D1%82%D0%B0%D1%86%D0%B8%D1%8F)
- [Рендеринг страницы](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D1%80%D0%B5%D0%BD%D0%B4%D0%B5%D1%80%D0%B8%D0%BD%D0%B3-%D1%81%D1%82%D1%80%D0%B0%D0%BD%D0%B8%D1%86%D1%8B)
- [GPU рендеринг](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#gpu-%D1%80%D0%B5%D0%BD%D0%B4%D0%B5%D1%80%D0%B8%D0%BD%D0%B3)
- [Windows server](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#windows-server)
- [Пост-рендеринг и выполнение, инициированное пользователем](https://github.com/thomasleverancier/WhatHappensWhen/blob/main/README.md#%D0%BF%D0%BE%D1%81%D1%82-%D1%80%D0%B5%D0%BD%D0%B4%D0%B5%D1%80%D0%B8%D0%BD%D0%B3-%D0%B8-%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8%D0%BD%D0%B8%D1%86%D0%B8%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D0%BE%D0%B5-%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D0%B5%D0%BC)

## Нажатие клавиши "g"

Следующие разделы объясняют физические действия клавиатуры и прерывания ОС. Когда вы нажимаете клавишу "g", браузер получает событие и запускаются функции автодополнения. В зависимости от алгоритма вашего браузера и того, находитесь ли вы в приватном/инкогнито режиме или нет, в выпадающем списке под адресной строкой будут представлены различные предложения. Большинство этих алгоритмов сортируют и приоритизируют результаты на основе истории поиска, закладок, куки и популярных поисков из интернета в целом. Пока вы печатаете "google.com", выполняется множество блоков кода, и предложения будут уточняться с каждым нажатием клавиши. Браузер может даже предложить "google.com" до того, как вы закончите его печатать.

## Клавиша "enter" нажимается до упора

Для выбора нулевой точки давайте выберем момент, когда клавиша Enter на клавиатуре достигает нижней границы своего хода. В этот момент замыкается электрическая цепь, специфичная для клавиши enter (либо напрямую, либо емкостно). Это позволяет небольшому количеству тока поступить в логическую схему клавиатуры, которая сканирует состояние каждого переключателя клавиши, подавляет электрические помехи от быстрого прерывистого замыкания переключателя и преобразует это в целое число кода клавиши, в данном случае 13. Затем контроллер клавиатуры кодирует код клавиши для передачи на компьютер. Сейчас это почти повсеместно происходит через соединение Universal Serial Bus (USB) или Bluetooth, но исторически это было через соединения PS/2 или ADB.

**В случае USB-клавиатуры:**

- USB-схема клавиатуры питается от источника питания 5В, подаваемого через контакт 1 от USB-контроллера компьютера.
- Сгенерированный код клавиши сохраняется внутренней схемой клавиатуры в памяти в регистре под названием "endpoint".
- USB-контроллер хоста опрашивает этот "endpoint" каждые ~10мс (минимальное значение, объявленное клавиатурой), поэтому он получает значение кода клавиши, сохраненное в нем.
- Это значение поступает в USB SIE (Serial Interface Engine) для преобразования в один или несколько USB-пакетов, которые следуют низкоуровневому USB-протоколу.
- Эти пакеты отправляются дифференциальным электрическим сигналом по контактам D+ и D- (средние 2) с максимальной скоростью 1.5 Мб/с, поскольку устройство HID (Human Interface Device) всегда объявляется как "низкоскоростное устройство" (соответствие USB 2.0).
- Затем этот последовательный сигнал декодируется USB-контроллером хоста компьютера и интерпретируется универсальным драйвером клавиатуры Human Interface Device (HID) компьютера. Значение клавиши затем передается в слой аппаратной абстракции операционной системы.

**В случае виртуальной клавиатуры (как в устройствах с сенсорным экраном):**

- Когда пользователь кладет палец на современный емкостный сенсорный экран, небольшое количество тока передается пальцу. Это замыкает цепь через электростатическое поле проводящего слоя и создает падение напряжения в этой точке экрана. Контроллер экрана затем вызывает прерывание, сообщая координаты нажатия клавиши.
- Затем мобильная ОС уведомляет текущее активное приложение о событии нажатия в одном из его GUI-элементов (который теперь является кнопками приложения виртуальной клавиатуры).
- Виртуальная клавиатура теперь может вызвать программное прерывание для отправки сообщения 'клавиша нажата' обратно в ОС.
- Это прерывание уведомляет текущее активное приложение о событии 'клавиша нажата'.

## Срабатывает прерывание [НЕ для USB-клавиатур]

Клавиатура посылает сигналы по своей линии запроса прерывания (IRQ), которая отображается на вектор прерывания (целое число) контроллером прерываний. CPU использует Таблицу Дескрипторов Прерываний (IDT) для отображения векторов прерываний на функции (обработчики прерываний), которые предоставляются ядром. Когда приходит прерывание, CPU индексирует IDT с вектором прерывания и запускает соответствующий обработчик. Таким образом, происходит вход в ядро.

## (В Windows) Приложению отправляется сообщение WM_KEYDOWN

HID-транспорт передает событие нажатия клавиши драйверу KBDHID.sys, который преобразует HID-использование в скан-код. В данном случае скан-код - VK_RETURN (0x0D). Драйвер KBDHID.sys взаимодействует с KBDCLASS.sys (драйвер класса клавиатуры). Этот драйвер отвечает за безопасную обработку всех входных данных клавиатуры и клавиатурной панели. Затем он вызывает Win32K.sys (после потенциальной передачи сообщения через сторонние фильтры клавиатуры, которые установлены). Все это происходит в режиме ядра.

Win32K.sys выясняет, какое окно является активным, через API GetForegroundWindow(). Этот API предоставляет дескриптор окна адресной строки браузера. Основной "насос сообщений" Windows затем вызывает SendMessage(hWnd, WM_KEYDOWN, VK_RETURN, lParam). lParam - это битовая маска, которая указывает дополнительную информацию о нажатии клавиши: количество повторов (0 в данном случае), фактический скан-код (может зависеть от OEM, но обычно не для VK_RETURN), были ли также нажаты расширенные клавиши (например, alt, shift, ctrl) (их не было), и некоторое другое состояние.

Windows API SendMessage - это простая функция, которая добавляет сообщение в очередь для конкретного дескриптора окна (hWnd). Позже основная функция обработки сообщений (называемая WindowProc), назначенная hWnd, вызывается для обработки каждого сообщения в очереди.

Окно (hWnd), которое активно, на самом деле является элементом управления редактированием, и WindowProc в этом случае имеет обработчик сообщений для сообщений WM_KEYDOWN. Этот код смотрит на 3-й параметр, который был передан в SendMessage (wParam) и, поскольку это VK_RETURN, знает, что пользователь нажал клавишу ENTER.

## (В OS X) Приложению отправляется NSEvent KeyDown

Сигнал прерывания запускает событие прерывания в I/O Kit kext драйвере клавиатуры. Драйвер переводит сигнал в код клавиши, который передается процессу OS X WindowServer. В результате WindowServer отправляет событие любым подходящим (например, активным или слушающим) приложениям через их Mach-порт, где оно помещается в очередь событий. События затем могут быть прочитаны из этой очереди потоками с достаточными привилегиями, вызывающими функцию mach_ipc_dispatch. Чаще всего это происходит через и обрабатывается основным циклом событий NSApplication через NSEvent типа NSEventType KeyDown.

## (В GNU/Linux) Xorg сервер прослушивает коды клавиш

Когда используется графический X-сервер, X будет использовать общий драйвер событий evdev для получения нажатия клавиши. Выполняется перемаппинг кодов клавиш в скан-коды с помощью специфичных для X-сервера карт клавиш и правил. Когда сканирование кода нажатой клавиши завершено, X-сервер отправляет символ оконному менеджеру (DWM, metacity, i3 и т.д.), поэтому оконный менеджер, в свою очередь, отправляет символ в сфокусированное окно. Графический API окна, которое получает символ, печатает соответствующий символ шрифта в соответствующем сфокусированном поле.

## Разбор URL

Теперь браузер имеет следующую информацию, содержащуюся в URL (Uniform Resource Locator):

- **Протокол** "http" - Использовать 'Hyper Text Transfer Protocol'
- **Ресурс** "/" - Получить главную (индексную) страницу

## Это URL или поисковый запрос?

Когда не указан протокол или действительное доменное имя, браузер переходит к передаче текста, введенного в адресную строку, в поисковую систему браузера по умолчанию. Во многих случаях к URL добавляется специальный фрагмент текста, чтобы сообщить поисковой системе, что он пришел из адресной строки конкретного браузера.

## Преобразование не-ASCII символов Unicode в имени хоста

Браузер проверяет имя хоста на наличие символов, которые не входят в a-z, A-Z, 0-9, -, или .. Поскольку имя хоста - google.com, их не будет, но если бы они были, браузер применил бы кодировку Punycode к части имени хоста в URL.

## Проверка списка HSTS

Браузер проверяет свой "предзагруженный список HSTS (HTTP Strict Transport Security)". Это список веб-сайтов, которые запросили связь только через HTTPS. Если веб-сайт находится в списке, браузер отправляет свой запрос через HTTPS вместо HTTP. В противном случае первоначальный запрос отправляется через HTTP. (Обратите внимание, что веб-сайт все еще может использовать политику HSTS без нахождения в списке HSTS. Первый HTTP-запрос к веб-сайту от пользователя получит ответ с требованием, чтобы пользователь отправлял только HTTPS-запросы. Однако этот единственный HTTP-запрос потенциально может оставить пользователя уязвимым для атаки понижения версии, поэтому список HSTS включен в современные веб-браузеры.)

## DNS-запрос

Браузер проверяет, находится ли домен в его кеше. (чтобы увидеть DNS-кеш в Chrome, перейдите по адресу chrome://net-internals/#dns). Если не найден, браузер вызывает библиотечную функцию gethostbyname (варьируется в зависимости от ОС) для выполнения поиска. gethostbyname проверяет, может ли имя хоста быть разрешено по ссылке в локальном файле hosts (местоположение которого варьируется в зависимости от ОС), прежде чем пытаться разрешить имя хоста через DNS. Если gethostbyname не имеет его в кеше и не может найти его в файле hosts, то он делает запрос к DNS-серверу, настроенному в сетевом стеке. Обычно это локальный маршрутизатор или кеширующий DNS-сервер интернет-провайдера. Если DNS-сервер находится в той же подсети, сетевая библиотека следует процессу ARP ниже для DNS-сервера. Если DNS-сервер находится в другой подсети, сетевая библиотека следует процессу ARP ниже для IP-адреса шлюза по умолчанию.

## Процесс ARP

Чтобы отправить ARP (Address Resolution Protocol) широковещательный запрос, библиотека сетевого стека должна знать целевой IP-адрес для поиска. Ей также нужно знать MAC-адрес интерфейса, который она будет использовать для отправки ARP-широковещания.

Сначала проверяется ARP-кеш на наличие ARP-записи для нашего целевого IP. Если она находится в кеше, библиотечная функция возвращает результат: Целевой IP = MAC.

Если запись не находится в ARP-кеше:

- Просматривается таблица маршрутизации, чтобы увидеть, находится ли целевой IP-адрес в любой из подсетей в локальной таблице маршрутизации. Если да, библиотека использует интерфейс, связанный с этой подсетью. Если нет, библиотека использует интерфейс, который имеет подсеть нашего шлюза по умолчанию.
- Ищется MAC-адрес выбранного сетевого интерфейса.
- Сетевая библиотека отправляет ARP-запрос уровня 2 (канальный уровень модели OSI):

**ARP-запрос:**

```
Sender MAC: interface:mac:address:here
Sender IP: interface.ip.goes.here
Target MAC: FF:FF:FF:FF:FF:FF (Broadcast)
Target IP: target.ip.goes.here
```

В зависимости от типа оборудования между компьютером и маршрутизатором:

**Прямое подключение:**

- Если компьютер подключен напрямую к маршрутизатору, маршрутизатор отвечает ARP-ответом (см. ниже)

**Концентратор:**

- Если компьютер подключен к концентратору, концентратор транслирует ARP-запрос из всех других портов. Если маршрутизатор подключен к тому же "проводу", он ответит ARP-ответом (см. ниже).

**Коммутатор:**

- Если компьютер подключен к коммутатору, коммутатор проверяет свою локальную CAM/MAC-таблицу, чтобы увидеть, на каком порту находится MAC-адрес, который мы ищем. Если у коммутатора нет записи для MAC-адреса, он ретранслирует ARP-запрос на все другие порты.
- Если у коммутатора есть запись в MAC/CAM-таблице, он отправит ARP-запрос на порт, который имеет MAC-адрес, который мы ищем.
- Если маршрутизатор находится на том же "проводе", он ответит ARP-ответом (см. ниже)

**ARP-ответ:**

```
Sender MAC: target:mac:address:here
Sender IP: target.ip.goes.here
Target MAC: interface:mac:address:here
Target IP: interface.ip.goes.here
```

Теперь, когда сетевая библиотека имеет IP-адрес либо нашего DNS-сервера, либо шлюза по умолчанию, она может возобновить свой DNS-процесс:

- DNS-клиент устанавливает сокет к UDP-порту 53 на DNS-сервере, используя исходный порт выше 1023.
- Если размер ответа слишком большой, вместо этого будет использоваться TCP.
- Если локальный/провайдерский DNS-сервер не имеет его, то запрашивается рекурсивный поиск, и это поднимается по списку DNS-серверов, пока не будет достигнут SOA, и если найден, возвращается ответ.

## Открытие сокета

Как только браузер получает IP-адрес сервера назначения, он берет его и данный номер порта из URL (HTTP-протокол по умолчанию использует порт 80, а HTTPS - порт 443) и делает вызов к системной библиотечной функции с именем socket и запрашивает TCP-сокет поток - AF_INET/AF_INET6 и SOCK_STREAM.

- Этот запрос сначала передается на транспортный уровень, где создается TCP-сегмент. Порт назначения добавляется к заголовку, а исходный порт выбирается из динамического диапазона портов ядра (ip_local_port_range в Linux).
- Этот сегмент отправляется на сетевой уровень, который оборачивает дополнительный IP-заголовок. IP-адрес сервера назначения, а также текущей машины вставляется для формирования пакета.
- Затем пакет прибывает на канальный уровень. Добавляется заголовок фрейма, который включает MAC-адрес сетевой карты машины, а также MAC-адрес шлюза (локального маршрутизатора). Как и раньше, если ядро не знает MAC-адрес шлюза, оно должно транслировать ARP-запрос, чтобы найти его.

В этот момент пакет готов к передаче через:

- Ethernet
- WiFi
- Сеть сотовой связи

Для большинства домашних или малых бизнес-подключений к интернету пакет пройдет от вашего компьютера, возможно, через локальную сеть, а затем через модем (MOdulator/DEModulator), который преобразует цифровые 1 и 0 в аналоговый сигнал, подходящий для передачи по телефонным, кабельным или беспроводным телефонным соединениям. На другом конце соединения находится другой модем, который преобразует аналоговый сигнал обратно в цифровые данные для обработки следующим сетевым узлом, где адреса отправителя и получателя будут дополнительно проанализированы.

Большинство крупных предприятий и некоторые новые жилые подключения будут иметь оптоволоконные или прямые Ethernet-соединения, в этом случае данные остаются цифровыми и передаются непосредственно следующему сетевому узлу для обработки.

В конце концов, пакет достигнет маршрутизатора, управляющего локальной подсетью. Оттуда он будет продолжать путешествовать к пограничным маршрутизаторам автономной системы (AS), другим AS и, наконец, к серверу назначения. Каждый маршрутизатор по пути извлекает адрес назначения из IP-заголовка и направляет его к соответствующему следующему узлу. Поле времени жизни (TTL) в IP-заголовке уменьшается на единицу для каждого проходящего маршрутизатора. Пакет будет отброшен, если поле TTL достигнет нуля или если текущий маршрутизатор не имеет места в своей очереди (возможно, из-за перегрузки сети).

Эта отправка и получение происходит несколько раз, следуя потоку TCP-соединения:

- Клиент выбирает начальный порядковый номер (ISN) и отправляет пакет серверу с установленным битом SYN, чтобы указать, что он устанавливает ISN
- Сервер получает SYN и если он в согласном настроении:
    - Сервер выбирает свой собственный начальный порядковый номер
    - Сервер устанавливает SYN, чтобы указать, что он выбирает свой ISN
    - Сервер копирует (клиентский ISN +1) в свое поле ACK и добавляет флаг ACK, чтобы указать, что он подтверждает получение первого пакета
- Клиент подтверждает соединение, отправляя пакет:
    - Увеличивает свой собственный порядковый номер
    - Увеличивает номер подтверждения получателя
    - Устанавливает поле ACK
- Данные передаются следующим образом:
    - Когда одна сторона отправляет N байтов данных, она увеличивает свой SEQ на это число
    - Когда другая сторона подтверждает получение этого пакета (или строки пакетов), она отправляет ACK-пакет со значением ACK, равным последнему полученному порядковому номеру от другой стороны
- Для закрытия соединения:
    - Закрывающая сторона отправляет FIN-пакет
    - Другая сторона подтверждает FIN-пакет и отправляет свой собственный FIN
    - Закрывающая сторона подтверждает FIN другой стороны с помощью ACK

## TLS рукопожатие

- Клиентский компьютер отправляет сообщение ClientHello серверу со своей версией Transport Layer Security (TLS), списком алгоритмов шифрования и доступных методов сжатия.
- Сервер отвечает сообщением ServerHello клиенту с версией TLS, выбранным шифром, выбранными методами сжатия и публичным сертификатом сервера, подписанным CA (Certificate Authority). Сертификат содержит публичный ключ, который будет использоваться клиентом для шифрования остальной части рукопожатия, пока не будет согласован симметричный ключ.
- Клиент проверяет цифровой сертификат сервера по своему списку доверенных CA. Если доверие может быть установлено на основе CA, клиент генерирует строку псевдослучайных байтов и шифрует ее публичным ключом сервера. Эти случайные байты могут быть использованы для определения симметричного ключа.
- Сервер расшифровывает случайные байты, используя свой приватный ключ, и использует эти байты для генерации своей собственной копии симметричного мастер-ключа.
- Клиент отправляет сообщение Finished серверу, шифруя хеш передачи до этого момента симметричным ключом.
- Сервер генерирует свой собственный хеш, а затем расшифровывает отправленный клиентом хеш, чтобы проверить, что он совпадает. Если да, он отправляет свое собственное сообщение Finished клиенту, также зашифрованное симметричным ключом.
- С этого момента TLS-сессия передает данные приложения (HTTP), зашифрованные согласованным симметричным ключом.

## Если пакет потерян

Иногда, из-за перегрузки сети или неисправных аппаратных соединений, TLS-пакеты будут потеряны до того, как они достигнут своего конечного пункта назначения. Отправитель затем должен решить, как реагировать. Алгоритм для этого называется управлением перегрузкой TCP. Это варьируется в зависимости от отправителя; наиболее распространенными алгоритмами являются cubic на более новых операционных системах и New Reno почти на всех остальных.

- Клиент выбирает окно перегрузки на основе максимального размера сегмента (MSS) соединения.
- Для каждого подтвержденного пакета окно удваивается в размере, пока не достигнет 'порога медленного старта'. В некоторых реализациях этот порог адаптивен.
- После достижения порога медленного старта окно увеличивается аддитивно для каждого подтвержденного пакета. Если пакет потерян, окно уменьшается экспоненциально, пока не будет подтвержден другой пакет.

## HTTP протокол

Если используемый веб-браузер был написан Google, вместо отправки HTTP-запроса для получения страницы, он отправит запрос на попытку согласования с сервером "обновления" с HTTP до протокола SPDY.

Если клиент использует HTTP-протокол и не поддерживает SPDY, он отправляет запрос серверу в форме:

```
GET / HTTP/1.1
Host: google.com
Connection: close
[другие заголовки]
```

где `[другие заголовки]` относится к серии разделенных двоеточием пар ключ-значение, отформатированных в соответствии со спецификацией HTTP и разделенных одиночными новыми строками. (Это предполагает, что используемый веб-браузер не имеет ошибок, нарушающих спецификацию HTTP. Это также предполагает, что веб-браузер использует HTTP/1.1, иначе он может не включать заголовок Host в запрос, и версия, указанная в GET-запросе, будет либо HTTP/1.0, либо HTTP/0.9.)

HTTP/1.1 определяет опцию соединения "close" для отправителя, чтобы сигнализировать, что соединение будет закрыто после завершения ответа. Например,

```
Connection: close
```

Приложения HTTP/1.1, которые не поддерживают постоянные соединения, ДОЛЖНЫ включать опцию соединения "close" в каждое сообщение.

После отправки запроса и заголовков веб-браузер отправляет одну пустую новую строку серверу, указывая, что содержимое запроса завершено.

Сервер отвечает кодом ответа, обозначающим статус запроса, и отвечает ответом в форме:

```
200 OK
[заголовки ответа]
```

За которым следует одна новая строка, а затем отправляет полезную нагрузку HTML-содержимого [www.google.com](http://www.google.com/). Сервер может затем либо закрыть соединение, либо, если заголовки, отправленные клиентом, запросили это, держать соединение открытым для повторного использования для дальнейших запросов.

Если HTTP-заголовки, отправленные веб-браузером, включали достаточную информацию для веб-сервера, чтобы определить, была ли версия файла, кешированного веб-браузером, неизмененной с момента последнего получения (т.е. если веб-браузер включил заголовок ETag), он может вместо этого ответить запросом в форме:

```
304 Not Modified
[заголовки ответа]
```

и без полезной нагрузки, и веб-браузер вместо этого извлекает HTML из своего кеша.

После разбора HTML веб-браузер (и сервер) повторяет этот процесс для каждого ресурса (изображение, CSS, favicon.ico и т.д.), на который ссылается HTML-страница, за исключением того, что вместо `GET / HTTP/1.1` запрос будет `GET /$(URL относительно www.google.com) HTTP/1.1`.

Если HTML ссылался на ресурс в другом домене, отличном от [www.google.com](http://www.google.com/), веб-браузер возвращается к шагам, связанным с разрешением другого домена, и следует всем шагам до этого момента для этого домена. Заголовок Host в запросе будет установлен на соответствующее имя сервера вместо google.com.

## Обработка HTTP-запроса сервером

HTTPD (HTTP Daemon) сервер - это тот, который обрабатывает запросы/ответы на стороне сервера. Наиболее распространенными HTTPD-серверами являются Apache или nginx для Linux и IIS для Windows.

- HTTPD (HTTP Daemon) получает запрос.
- Сервер разбивает запрос на следующие параметры:
    - HTTP-метод запроса (либо GET, HEAD, POST, PUT, PATCH, DELETE, CONNECT, OPTIONS, или TRACE). В случае URL, введенного непосредственно в адресную строку, это будет GET.
    - Домен, в данном случае - google.com.
    - Запрашиваемый путь/страница, в данном случае - / (поскольку не был запрошен конкретный путь/страница, / является путем по умолчанию).
- Сервер проверяет, что на сервере настроен виртуальный хост, который соответствует google.com.
- Сервер проверяет, что google.com может принимать GET-запросы.
- Сервер проверяет, что клиенту разрешено использовать этот метод (по IP, аутентификации и т.д.).
- Если на сервере установлен модуль перезаписи (как mod_rewrite для Apache или URL Rewrite для IIS), он пытается сопоставить запрос с одним из настроенных правил. Если найдено соответствующее правило, сервер использует это правило для перезаписи запроса.
- Сервер переходит к извлечению содержимого, которое соответствует запросу, в нашем случае он вернется к индексному файлу, поскольку "/" является основным файлом (некоторые случаи могут переопределить это, но это наиболее распространенный метод).
- Сервер разбирает файл в соответствии с обработчиком. Если Google работает на PHP, сервер использует PHP для интерпретации индексного файла и передает вывод клиенту.

## За кулисами браузера

Как только сервер предоставляет ресурсы (HTML, CSS, JS, изображения и т.д.) браузеру, он проходит через следующий процесс:

- Парсинг - HTML, CSS, JS
- Рендеринг - Построение DOM-дерева → Дерево рендеринга → Компоновка дерева рендеринга → Раскраска дерева рендеринга

## Браузер

Функциональность браузера заключается в представлении выбранного вами веб-ресурса, запрашивая его с сервера и отображая его в окне браузера. Ресурс обычно является HTML-документом, но может также быть PDF, изображением или каким-либо другим типом контента. Местоположение ресурса указывается пользователем с помощью URI (Uniform Resource Identifier).

Способ, которым браузер интерпретирует и отображает HTML-файлы, указан в спецификациях HTML и CSS. Эти спецификации поддерживаются организацией W3C (World Wide Web Consortium), которая является организацией стандартов для веба.

Пользовательские интерфейсы браузеров имеют много общего друг с другом. Среди общих элементов пользовательского интерфейса:

- Адресная строка для вставки URI
- Кнопки назад и вперед
- Опции закладок
- Кнопки обновления и остановки для обновления или остановки загрузки текущих документов
- Кнопка домой, которая переводит вас на вашу домашнюю страницу

**Высокоуровневая структура браузера**

Компоненты браузеров:

- **Пользовательский интерфейс:** Пользовательский интерфейс включает адресную строку, кнопку назад/вперед, меню закладок и т.д. Каждая часть отображения браузера, кроме окна, где вы видите запрошенную страницу.
- **Движок браузера:** Движок браузера управляет действиями между UI и движком рендеринга.
- **Движок рендеринга:** Движок рендеринга отвечает за отображение запрошенного контента. Например, если запрошенный контент - HTML, движок рендеринга разбирает HTML и CSS и отображает разобранный контент на экране.
- **Сеть:** Сеть обрабатывает сетевые вызовы, такие как HTTP-запросы, используя различные реализации для разных платформ за платформо-независимым интерфейсом.
- **UI бэкенд:** UI бэкенд используется для рисования базовых виджетов, таких как комбо-боксы и окна. Этот бэкенд предоставляет общий интерфейс, который не является платформо-специфичным. Под ним он использует методы пользовательского интерфейса операционной системы.
- **JavaScript движок:** JavaScript движок используется для разбора и выполнения JavaScript-кода.
- **Хранилище данных:** Хранилище данных - это слой персистентности. Браузер может нуждаться в сохранении всех видов данных локально, таких как куки. Браузеры также поддерживают механизмы хранения, такие как localStorage, IndexedDB, WebSQL и FileSystem.

## HTML парсинг

Движок рендеринга начинает получать содержимое запрошенного документа из сетевого слоя. Обычно это делается порциями по 8кБ.

Основная задача HTML-парсера - разобрать HTML-разметку в дерево разбора.

Выходное дерево ("дерево разбора") - это дерево DOM-элементов и узлов атрибутов. DOM - это сокращение от Document Object Model. Это объектное представление HTML-документа и интерфейс HTML-элементов к внешнему миру, такому как JavaScript. Корень дерева - объект "Document". До любых манипуляций через скрипты DOM имеет почти взаимно-однозначное отношение к разметке.

**Алгоритм разбора**

HTML не может быть разобран с использованием обычных нисходящих или восходящих парсеров.

Причины:

- Прощающая природа языка.
- Тот факт, что браузеры имеют традиционную толерантность к ошибкам для поддержки хорошо известных случаев недействительного HTML.
- Процесс разбора является реентерабельным. Для других языков источник не изменяется во время разбора, но в HTML динамический код (такой как элементы скрипта, содержащие вызовы document.write()) может добавлять дополнительные токены, поэтому процесс разбора фактически модифицирует ввод.

Не имея возможности использовать обычные техники разбора, браузер использует пользовательский парсер для разбора HTML. Алгоритм разбора подробно описан в спецификации HTML5.

Алгоритм состоит из двух этапов: токенизация и построение дерева.

**Действия по завершении разбора**

Браузер начинает загружать внешние ресурсы, связанные со страницей (CSS, изображения, JavaScript-файлы и т.д.).

На этом этапе браузер помечает документ как интерактивный и начинает разбор скриптов, которые находятся в "отложенном" режиме: тех, которые должны быть выполнены после разбора документа. Состояние документа устанавливается в "complete", и запускается событие "load".

Обратите внимание, что на HTML-странице никогда не бывает ошибки "Invalid Syntax". Браузеры исправляют любой недействительный контент и продолжают.

## CSS интерпретация

- Разбор CSS-файлов, содержимого тегов `<style>` и значений атрибутов `style`, используя "CSS лексическую и синтаксическую грамматику"
- Каждый CSS-файл разбирается в объект StyleSheet, где каждый объект содержит CSS-правила с селекторами и объектами, соответствующими CSS-грамматике.
- CSS-парсер может быть нисходящим или восходящим, когда используется конкретный генератор парсера.

## Рендеринг страницы

- Создание 'Дерева фреймов' или 'Дерева рендеринга' путем обхода DOM-узлов и вычисления значений CSS-стилей для каждого узла.
- Вычисление предпочтительной ширины каждого узла в 'Дереве фреймов' снизу вверх путем суммирования предпочтительной ширины дочерних узлов и горизонтальных отступов, границ и заполнения узла.
- Вычисление фактической ширины каждого узла сверху вниз путем распределения доступной ширины каждого узла его дочерним элементам.
- Вычисление высоты каждого узла снизу вверх путем применения переноса текста и суммирования высот дочерних узлов и отступов, границ и заполнения узла.
- Вычисление координат каждого узла, используя информацию, вычисленную выше.
- Более сложные шаги предпринимаются, когда элементы плавающие, позиционированы абсолютно или относительно, или используются другие сложные функции. См. [http://dev.w3.org/csswg/css2/](http://dev.w3.org/csswg/css2/) и [http://www.w3.org/Style/CSS/current-work](http://www.w3.org/Style/CSS/current-work) для более подробной информации.
- Создание слоев для описания того, какие части страницы могут быть анимированы как группа без повторной растеризации. Каждый фрейм/объект рендеринга назначается слою.
- Текстуры выделяются для каждого слоя страницы.
- Фрейм/объекты рендеринга для каждого слоя обходятся, и команды рисования выполняются для их соответствующего слоя. Это может быть растеризовано CPU или нарисовано на GPU напрямую, используя D2D/SkiaGL.
- Все вышеперечисленные шаги могут повторно использовать вычисленные значения с последнего раза, когда веб-страница была отрендерена, так что инкрементальные изменения требуют меньше работы.
- Слои страницы отправляются в процесс композитинга, где они объединяются со слоями для другого видимого контента, такого как хром браузера, iframe и панели дополнений.
- Вычисляются финальные позиции слоев, и команды композита выдаются через Direct3D/OpenGL. Буфер(ы) команд GPU сбрасываются в GPU для асинхронного рендеринга, и фрейм отправляется в оконный сервер.

## GPU рендеринг

Во время процесса рендеринга графические вычислительные слои могут использовать CPU общего назначения или графический процессор GPU.

При использовании GPU для графических вычислений рендеринга графические программные слои разделяют задачу на несколько частей, чтобы воспользоваться массивным параллелизмом GPU для вычислений с плавающей точкой, необходимых для процесса рендеринга.

## Windows server

## Пост-рендеринг и выполнение, инициированное пользователем

После завершения рендеринга браузер выполняет JavaScript-код в результате какого-либо механизма времени (такого как анимация Google Doodle) или взаимодействия с пользователем (ввод запроса в поисковое поле и получение предложений). Плагины, такие как Flash или Java, также могут выполняться, хотя не в это время на домашней странице Google. Скрипты могут вызывать дополнительные сетевые запросы, а также изменять страницу или ее макет, вызывая еще один раунд рендеринга и раскраски страницы.
