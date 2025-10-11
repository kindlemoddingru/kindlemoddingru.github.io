---
layout: default
parent: Джейлбрейк вашего Kindle
title: WinterBreak
nav_order: 4
---

# WinterBreak
<a href='https://ko-fi.com/hackerdude' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://storage.ko-fi.com/cdn/brandasset/v2/support_me_on_kofi_dark.png' border='0' alt='Buy Me a Coffee at ko-fi.com' />

> After all, all devices have their dangers. The discovery of speech introduced communication – and lies.
> <br/>
> \- Isaac Asimov

WinterBreak — это джейлбрейк, выпущенный в Новый год 2025 года пользователем [HackerDude](https://www.mobileread.com/forums/member.php?u=330416)

Он основан на [Mesquito](../../mesquito/)

{: .note}
> Особая благодарность Marek, NiLuJe, Katadelos и всем бета-тестерам, участвовавшим в разработке этого джейлбрейка.  
>
> R.I.P. брикнутые Kindle во время тестирования  
> <br/>
> R.I.P. оригинальные дедлайны

## Необходимые условия
- Вам понадобится компьютер (ПК)
- Ваш Kindle должен быть зарегистрирован
- Ваш Kindle должен иметь сохранённую действующую Wi-Fi сеть с доступом в интернет, к которой он сможет подключиться на шагах с 8 по 10 (включительно)
- Программа для распаковки архивов ([7-zip](https://www.7-zip.org/) или [WinRar](https://www.win-rar.com/start.html?&L=0) для Windows)

{: .highlight}
Если вы столкнулись с проблемами, обратитесь к разделу [Устранение неполадок](#troubleshooting)

## Руководство по установке

<div id="guide">
    <div class="buttons">
        <button class="btn btn-orange" id="prev">Предыдущий шаг</button>
        <span id="stepCounter"></span>
        <button class="btn btn-green" id="next">Следующий шаг</button>
    </div>
    <div id="stepwrapper" class="stepwrapper">
        <div class="step">
            <h2>Скачайте последнюю версию WinterBreak:</h2>
            <div class="stepContent">
                <a href="https://github.com/KindleModding/WinterBreak/releases/latest/download/WinterBreak.tar.gz" class="btn btn-purple">Скачать</a>
                <p class="note">
                    Если ваш Kindle <b>ещё не зарегистрирован</b>, обязательно следуйте <a href="../prevent-auto-update.html">этим шагам, чтобы предотвратить автоматическое обновление</a> перед регистрацией устройства на Amazon. Это поможет избежать автоматического обновления прошивки во время регистрации.
                </p>
                <p class="warning">
                    WinterBreak/Mesquito НЕ работают на прошивках версии <code>5.18.1</code> и выше.
                </p>
            </div>
        </div>
        <div class="step">
            <h2>Режим «В самолёте»</h2>
            <div class="stepContent">
                <p>Включите на Kindle режим «В самолёте»</p>
                <img src="./airplane_mode.png" /> 
            </div>
        </div>
        <div class="step">
            <h2>Перезагрузка</h2>
            <div class="stepContent">
                <p>Перезагрузите Kindle</p>
                <img src="./reboot.png" />
            </div>
        </div>
        <div class="step">
            <h2>Распаковка WinterBreak</h2>
            <div class="stepContent">
                <p>После загрузки устройства подключите Kindle к компьютеру и распакуйте содержимое архива <code>WinterBreak.tar.gz</code> в удобное место на компьютере</p>
                <p>Затем скопируйте файлы на Kindle (не распаковывайте напрямую на устройство — это может привести к ошибке). Замените файлы, если система попросит подтверждение</p>
                <p class="highlight">
                    Пользователи Linux/MacOS: УБЕДИТЕСЬ, что скрытая папка <code>.active_content_sandbox</code> была скопирована на Kindle
                </p>
                <img src="./file_list.png" />
            </div>
        </div>
        <div class="step">
            <h2>Запуск Mesquito</h2>
            <div class="stepContent">
                <p>Безопасно отключите Kindle от компьютера</p>
                <p>Откройте магазин Kindle на устройстве, нажав на иконку корзины на главном экране</p>
                <p>При запросе подтвердите, нажав <code>Yes</code>, чтобы выключить режим «В самолёте»</p>
                <img src="./store_aeroplane.png" />
            </div>
        </div>
        <div class="step">
            <h2>Запуск WinterBreak</h2>
            <div class="stepContent">
                <p>После загрузки Mesquito нажмите на иконку WinterBreak</p>
                <img src="./winterbreak_launcher.png" />
            </div>
        </div>
        <div class="step">
            <h2>Готово</h2>
            <div class="stepContent">
                <p>Подождите около 30 секунд — Kindle должен показать сообщение вроде «Now you are ready to install the hotfix»</p>
                <p>Если текст не появился, повторите шаги ещё раз. Как только появится сообщение, <b>включите обратно режим «В самолёте»</b> и переходите к этапу после джейлбрейка.
                </p>
                <p class="warning">
                    Если существует файл <code>update.bin.tmp.partial</code>, удалите его, чтобы предотвратить автоматическое обновление.
                </p>
                <img src="./winterbreak_run.png" />
            </div>
        </div>
    </div>
    <div class="buttons">
        <button class="btn btn-orange" id="prev">Предыдущий шаг</button>
        <span id="stepCounter"></span>
        <button class="btn btn-green" id="next">Следующий шаг</button>
    </div>
</div>
<script>new Guide("guide", "../post-jailbreak/setting-up-a-hotfix", "Настройка Hotfix");</script>

# Устранение неполадок

Если при попытке войти в Kindle Store возникает ошибка **«Unexpected error»** или отображается только главная страница магазина, попробуйте следующие решения:

### Замена LocalStorage

1. После успешной регистрации подключите Kindle к ПК и удалите папку `.active_content_sandbox`. Также удалите любые файлы с именем вроде `update.bin.tmp.partial`, чтобы предотвратить автоматическое обновление.
2. Перезагрузите Kindle
3. Отключите режим «В самолёте» и подключитесь к Wi-Fi
4. Откройте обычный магазин Kindle и проведите там несколько минут — просматривайте категории книг и скачайте бесплатный образец любой книги, чтобы сгенерировать нужные файлы
5. Через несколько минут снова включите режим «В самолёте» и подключите Kindle к ПК
6. Удалите папку кэша по пути `.active_content_sandbox/store/resource/LocalStorage`. Если папка ещё не появилась, побудьте в Kindle Store ещё несколько минут, пока она не создастся. Не забудьте удалить файл `update.bin.tmp.partial` перед каждой перезагрузкой.
7. После удаления скопируйте файлы WinterBreak на Kindle и перезагрузите устройство
8. Откройте Kindle Store, при запросе нажмите `Yes`, чтобы выключить режим «В самолёте»

### Сброс к заводским настройкам
> Ошибка и её решение найдены пользователями [DiabloSat](https://github.com/progzone122) и [Rexathion1](https://github.com/Rexathion1)

1. Выполните сброс Kindle до заводских настроек
2. Перед регистрацией — подключите Kindle к ПК и переместите файлы WinterBreak в корень устройства
3. Войдите в свою учётную запись и как можно скорее включите режим «В самолёте»
4. Подключите Kindle к ПК и удалите папку кэша по пути `.active_content_sandbox/store/resource/LocalStorage` (пропустите шаг, если папка `LocalStorage` не существует)
5. Перезагрузите Kindle
6. Откройте Kindle Store на устройстве
7. При запросе нажмите `Yes`, чтобы выключить режим «В самолёте»

# Особая благодарность нашим отважным бета-тестерам

- Crystals (брикнул свой PW4 во время тестирования)
- mergen3107 (придумал название "WinterBreak")
- Bomberfish
- BionicGecko
- Juliet
- Rie
- Robotic
- scrad
- shamanNS
- akane
- BlackNinja
- Gimzie
- Elaine Roberts
- Lux
- Marek
- terra
