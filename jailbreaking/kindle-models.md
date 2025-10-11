---
layout: default
parent: Джейлбрейк вашего Kindle
title: Модели Kindle
nav_order: 2
---

# Модели Kindle

{: .highlight }
Вы можете найти серийный номер вашего Kindle, перейдя в `Настройки` > `Параметры устройства` > `Информация об устройстве`.  
Там откроется окно, в котором вы сможете увидеть серийный номер вашего Kindle.

{: .highlight }
Вам нужно ввести только первые 8 символов серийного номера, а не все 16 символов.

<div style="display: flex; flex-direction: column; justify-content: center; align-items: center;">
    <h3>Введите серийный номер вашего Kindle</h3>
    <p id="searchStatus"></p>
    <input type="text" id="serialNumber" onchange="searchForSerial()" style="width: 100%; height: 100%; padding: 0.5rem 1rem 0.5rem 2.5rem; font-size: 16px; color: #e6e1e8; background-color: #302d36; border-top: 0; border-right: 0; border-bottom: 0; border-left: 0; border-radius: 0; text-align: center;">
    <button class="btn" style="margin-top: 0.5em;" onclick="searchForSerial()">Найти модель</button>
</div>

<div id="searchResult">
</div>

<div>
<h2>Все модели Kindle</h2>
<div id="fullModelTable" class="table-wrapper"></div>
</div>


<script src="./modelFinder.js"></script>