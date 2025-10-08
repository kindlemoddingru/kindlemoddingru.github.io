---
layout: default
parent: Джейлбрейк вашего Kindle
title: AdBreak
nav_order: 3
---

# AdBreak

> Если я не могу делать великие дела, я могу делать маленькие дела по-великому.
> <br/>
> \- Мартин Лютер Кинг, младший

AdBreak — это джейлбрейк, выпущенный 24/09/2025 пользователем hhhhhhhhh.

Он основан на [CVE-2012-3748](https://scarybeastsecurity.blogspot.com/2017/05/ode-to-use-after-free-one-vulnerable.html).

{: .note}
> Для устройств Scribe нужно использовать французский аккаунт, чтобы включить рекламу

{: .note}
> Особая благодарность Chris Evans (@scarybeasts) за большую часть кода эксплойта и hackerdude за модифицированный JB-скрипт.

## Требования

- Потребуется ПК, кабель
- Kindle с рекламой, зарегистрированный и не в чёрном списке
- Прошивка 5.18.1 и выше (возможно, не работает после 5.18.5.0.1)

{: .highlight}
Если возникнут проблемы, см. раздел [Устранение неполадок](#troubleshooting). Там также есть информация о том, как снова включить рекламу на Kindle, где она отключена.

## Руководство по установке

<div id="guide">
    <div class="buttons">
        <button class="btn btn-orange" id="prev">Предыдущий шаг</button>
        <span id="stepCounter"></span>
        <button class="btn btn-green" id="next">Следующий шаг</button>
    </div>
    <div id="stepwrapper" class="stepwrapper">
        <div class="step">
            <h2>Скачайте последнюю версию AdBreak:</h2>
            <div class="stepContent">
                <a href="https://github.com/htimesnine/AdBreak/releases/download/v1.0.1/adbreak.zip" class="btn btn-purple">Скачать</a>
                <p class="note">
                    Если ваш Kindle <b>ещё не зарегистрирован</b>, обязательно выполните <a href="../prevent-auto-update.html">эти шаги, чтобы предотвратить автоматическое обновление</a> перед регистрацией устройства на Amazon. Это поможет избежать автоматического обновления прошивки во время регистрации.
                </p>
                <p class="warning">
                    Используйте WinterBreak на прошивках <code>5.18.0.2</code> и ниже.
                </p>
            </div>
        </div>
        <div class="step">
            <h2>Скачайте рекламу</h2>
            <div class="stepContent">
                <p>Оставьте Kindle подключённым к интернету, чтобы он скачал рекламные объявления.<br/><br/> Если нажать кнопку блокировки, должно появиться рекламное изображение.<br/><br/> Если реклама не появляется, попробуйте сброс к заводским настройкам.</p>
            </div>
        </div>
        <div class="step">
            <h2>Режим полёта</h2>
            <div class="stepContent">
                <p>После того как убедились, что реклама отображается на экране блокировки, включите режим полёта.</p>
                <img src="./airplane_mode.png" /> 
            </div>
        </div>
        <div class="step">
            <h2>Просмотр всех объявлений</h2>
            <div class="stepContent">
                <p>Нажмите на меню в правом верхнем углу и выберите "View all ads", чтобы увидеть несколько "special offers".</p>
                <img src="./view_ads.png" />
            </div>
        </div>
        <div class="step">
            <h2>Скопируйте .assets</h2>
            <div class="stepContent">
                <p>Подключите Kindle, откройте системную папку и скопируйте папку ".assets" на компьютер.</p>
                <img src="./copy_assets.png" />
            </div>
        </div>
        <div class="step">
            <h2>Распакуйте AdBreak</h2>
            <div class="stepContent">
                <p>Распакуйте ранее скачанный AdBreak и поместите содержимое внутрь папки ".assets" на компьютере.</p>
                <img src="./copy_adbreak.png" />
            </div>
        </div>
        <div class="step">
            <h2>Запустите скрипт замены</h2>
            <div class="stepContent">
                <div class="version-block">
                    <p class="version-label">Windows:</p>
                    <p>Дважды кликните на "replace.bat" для запуска.</p>
                </div>
                <div class="version-block">
                    <p class="version-label">MacOS/Linux:</p>
                    <p>В терминале выполните <code> find . -name 'details.html' -exec cp adbreak.html {} \;</code>.</p>
                </div>
                <img src="./replacer.png" />
            </div>
        </div>
        <div class="step">
            <h2>Замените .assets на Kindle</h2>
            <div class="stepContent">
                <p>Удалите оригинальную папку Kindle <code>.assets</code> и замените её модифицированной копией с компьютера.</p>
                <img src="./replace_old_assets.png" />
            </div>
        </div>
        <div class="step">
            <h2>Джейлбрейк!</h2>
            <div class="stepContent">
                <p>Отключите устройство, нажмите на рекламное объявление и пройдите через всплывающие окна. После нажатия Close на "Bang!" скрипт джейлбрейка должен запуститься.</p>
                <p class="note">
                    Сообщения об ошибках приложений можно безопасно игнорировать, они не имеют значения.
                </p>
                <img src="./demo.png" />
            </div>
        </div>
    </div>
    <div class="buttons">
        <button class="btn btn-orange" id="prev">Предыдущий шаг</button>
        <span id="stepCounter"></span>
        <button class="btn btn-green" id="next">Следующий шаг</button>
    </div>
</div>
<script>new Guide("guide", "../post-jailbreak/setting-up-a-hotfix", "Установка хотфикса");</script>

<style>
.version-block {
    background-color: #1e1e1e;
    border-radius: 8px;
    padding: 12px;
    margin-bottom: 12px;
    width: 100%;
}

.version-label {
    font-weight: bold;
    border-bottom: 1px solid #369d36;
    padding-bottom: 5px;
    margin-bottom: 10px;
    color: #369d36;
}
</style>

## Устранение неполадок

### Часто задаваемые вопросы

- Джейлбрейк НЕ удаляет рекламу автоматически, см. скрипт Marek.  
- Никогда не сработает на CS/Colorsoft! Рекламу там включить нельзя!  
- Нет, это не "UJ"/"Unnamed Jailbreak". Это отдельный проект.  
- "Можно ли сделать устройство поддерживающим рекламу?" (см. ниже)

### Частые проблемы

- Не могу найти системную папку:  
    - На Kindle с массовым хранилищем, **если не видно `system`**, нужно перейти к пути вручную или следовать [этой инструкции](https://kb.blackbaud.com/knowledgebase/Article/41890) для отображения защищённых системных папок.
- Появляется "Bang!", но джейлбрейк не запускается:  
    - Проверьте папку .assets на Kindle. В ней должны быть "jb.sh" и "patchedUks.sqsh".

### Включение рекламы
(требуется для джейлбрейка, можно удалить позже)

- Смените регион аккаунта  
   - Перейдите Manage Your Content and Devices → Preferences → Country/Region Settings → Change.  
   - Выберите: US, UK, DE, FR, IT, ES, JP, CN  
   - Укажите корректные данные (адрес, телефон, e-mail).

- Добавьте способ оплаты  
   - Установите карту и адрес по выбранному региону.  
   - Деньги не будут сняты.

- Включите специальные предложения  
   - В аккаунте Amazon включите Special Offers для Kindle.

- Синхронизируйте Kindle  
   - Подключитесь к Wi-Fi, реклама появится на экране блокировки.

Примечания:  
- Если Kindle изначально был без рекламы, повторное отключение бесплатно.  
- Если Kindle с рекламой, отключение обычно платное, но после JB можно удалить скриптом.

## Особая благодарность

- Penguins184: это руководство  
- Ceoz: исследования по включению рекламы
