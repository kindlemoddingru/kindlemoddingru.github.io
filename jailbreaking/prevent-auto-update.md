---
layout: default
parent: Джейлбрейк вашего Kindle
title: Предотвращение автоматических обновлений
nav_order: 99
has_children: true
---

# Предотвращение автоматических обновлений через заполнение памяти Kindle

## Зачем заполнять память Kindle?

Устройства Kindle могут автоматически загружать и устанавливать обновления прошивки, если у них достаточно свободного места. Эти обновления могут заблокировать возможность джейлбрейка. Автоматические обновления происходят, когда:

- Вы открываете магазин Kindle.
- Вы регистрируете Kindle на аккаунт Amazon.
- Устройство подключается к Wi-Fi, даже на короткое время.
- Kindle перезагружается при подключённом интернете.

Если заполнить память устройства (оставив только 50–200 МБ свободного места), Kindle не сможет загрузить и установить обновление, так как для этого требуется больше свободного пространства.

## Как заполнить память Kindle

{: .warning}
> Удалите файлы `update-whatever.bin` ИЛИ `update.partial.bin` и включите режим полёта!

Можно воспользоваться простым скриптом, который заполнит память Kindle «пустыми» файлами, оставив немного свободного места. Скрипт доступен в [репозитории Kindle-Filler-Disk на GitHub](https://github.com/bastianmarin/Kindle-Filler-Disk/) — там же есть версии для Windows, macOS и Linux.

{: .note}
> Скрипт не работает на Kindle 11-го поколения и новее, так как они подключаются к компьютеру через MTP.
>
> В этом случае у вас есть два варианта:
> 1. 1. На каждом этапе руководства по джейлбрейку вручную удалять все файлы, оканчивающиеся на <code>.bin</code>, или с именем вроде <code>update.bin.tmp.partial</code>.
> 2. Заполнить Kindle вручную. Скачайте [файлы-заполнители](https://github.com/bastianmarin/Kindle-Filler-Disk/tree/main/MTP/), соответствующие объёму памяти вашего Kindle, распакуйте их и перенесите в корень устройства (можно в отдельную папку). После этого убедитесь, что свободного места осталось 50–200 МБ.


<div id="guide">
    <div class="buttons">
        <button class="btn btn-orange" id="prev">Предыдущий шаг</button>
        <span id="stepCounter"></span>
        <button class="btn btn-green" id="next">Следующий шаг</button>
    </div>
    <div id="stepwrapper" class="stepwrapper">
        <div class="step">
            <h2>1. Включите режим полёта</h2>
            <div class="stepContent">
                <p>На Kindle включите режим полёта</p>
                <img src="./WinterBreak/airplane_mode.png" />
            </div>
        </div>
        <div class="step">
            <h2>2. Подключите Kindle к компьютеру через USB</h2>
            <div class="stepContent">
                <p>Используйте USB-кабель для подключения Kindle к компьютеру.</p>
                <img src="./Prevent/usb-mode.png"/>
                <p>Дождитесь, пока устройство появится как USB-диск.</p>
            </div>
        </div>
        <div class="step">
            <h2>3. Скачайте скрипт для заполнения памяти</h2>
            <div class="stepContent">
                <p>Перейдите в <a href="https://github.com/bastianmarin/Kindle-Filler-Disk/">репозиторий Kindle-Filler-Disk на GitHub</a>.</p>
                <img src="./Prevent/github-files.png"/>
                <p>Скачайте подходящий скрипт для вашей операционной системы:</p>
                <div style="margin-left:2em">
                    <span><strong>Windows:</strong> <code>Filler.ps1</code></span><br/>
                    <span><strong>macOS/Linux:</strong> <code>Filler.sh</code></span>
                </div>
            </div>
        </div>
        <div class="step">
            <h2>4. Перенесите скрипт на Kindle</h2>
            <div class="stepContent">
                <p>Скопируйте скачанный файл в корневую папку Kindle (главная директория, которая открывается при подключении устройства).</p>
                <img src="./Prevent/root-main.png"/>
                <span><strong>Windows:</strong> <code>Filler.ps1</code></span><br/>
                <span><strong>macOS/Linux:</strong> <code>Filler.sh</code></span>
            </div>
        </div>
        <div class="step">
            <h2>5. Запустите скрипт</h2>
            <div class="stepContent">
                <div class="version-block">
                    <p class="version-label">Windows:</p>
                    <p>Откройте проводник и перейдите к диску Kindle.</p>
                    <p>Кликните правой кнопкой по <code>Filler.ps1</code> и выберите <strong>Run with PowerShell</strong>.</p>
                    <p>Если появится ошибка политики выполнения, откройте PowerShell в папке Kindle и выполните:</p>
                    <pre><code>powershell -ExecutionPolicy Bypass -File .\Filler.ps1</code></pre>
                </div>
                <div class="version-block">
                    <p class="version-label">macOS/Linux:</p>
                    <p>Откройте терминал в папке, где находится <code>Filler.sh</code>.</p>
                    <p>Сделайте файл исполняемым, если нужно:</p>
                    <pre><code>chmod +x Filler.sh</code></pre>
                    <p>Запустите скрипт:</p>
                    <pre><code>./Filler.sh</code></pre>
                </div>
                <img src="./Prevent/run-script.png"/>
              </div>     
            </div>
        <div class="step">
            <h2>6. Безопасно извлеките и проверьте память</h2>
            <div class="stepContent">
                <p>Извлеките Kindle из компьютера.</p>
                <p>На устройстве откройте <strong>Настройки &gt; Параметры устройства &gt; Информация об устройстве</strong>.</p>
                <p>Убедитесь, что доступно <strong>20 МБ или меньше</strong> свободного места.</p>
                <img src="./Prevent/final.png"/>
            </div>
        </div>
        <div class="step">
            <h2>7. Зарегистрируйте Kindle</h2>
            <div class="stepContent">
                <p>При почти заполненной памяти подключите Kindle к Wi-Fi и зарегистрируйте его в аккаунте Amazon. Обновление не скачается из-за нехватки места.</p>
            </div>
        </div>
        <div class="step">
            <h2>8. Снова включите режим полёта</h2>
            <div class="stepContent">
                <p>Сразу после регистрации снова включите <strong>режим полёта</strong>, чтобы предотвратить попытки обновления.</p>
                <p>Теперь можно переходить к следующим шагам джейлбрейка (например, WinterBreak).</p>
                <p class="highlight">
                    <strong>Важно:</strong> после заполнения памяти Kindle проверьте содержимое <strong>корневой папки</strong> и удалите все файлы, оканчивающиеся на <code>.bin</code> или с именем <code>update.bin.tmp.partial</code>. Это файлы автоматических обновлений — их нужно удалить, чтобы Kindle не пытался установить обновление при освобождении памяти.
                </p>
            </div>
        </div>
    </div>
    <div class="buttons">
        <button class="btn btn-orange" id="prev">Предыдущий шаг</button>
        <span id="stepCounter"></span>
        <button class="btn btn-green" id="next">Следующий шаг</button>
    </div>
</div>

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

<script>new Guide("guide", "./getting-started", "Jailbreak");</script>

---

## После джейлбрейка: освобождение памяти

После завершения джейлбрейка вы можете удалить папку `fill_disk`, чтобы вернуть свободное место.  
Можно также удалить только часть файлов, если вы хотите, чтобы память оставалась почти заполненной.

- **Windows:**  
  Откройте проводник и найдите папку `fill_disk`. Удалите её полностью или только часть файлов внутри.

- **Linux / macOS:**  
  Откройте терминал в папке с `fill_disk` и выполните:
  ```sh
  rm -rf fill_disk