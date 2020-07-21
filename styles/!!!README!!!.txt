How to use:

1. Use QGIS 1.7 or higher.
2. Go to Settings->Style manager.
3. Hit "Import" button.
4. Provide path to the "symbology-ng-style-eng.xml" file in this archive.
5. Pick up needed symbols or choose all of them and hit "Import" button.

Note that there should not be any red circles in symbols after import is complete. 
If you will see red circles (or do not see some of the symbols despite their names
present) it means that paths to some of the SVG icons are broken. 
You should fix them manually by editing "symbology-ng-style.xml" file LOCATED AT YOUR 
USRER'S QGIS FOLDER by copying according paths from "symbology-ng-style-eng.xml" file FROM THIS ARCHIVE.

---------------------------------------------

Как пользоваться набором символов:

1. Используйте QGIS 1.7 или более позднюю версию.
2. Скопируйте содержимое директории svg/ в директорию со значками qgis (Linux: /usr/share/qgis/svg; Windows: OSGeo4W\apps\qgis\svg), 
   или добавьте путь к ней в настройках (Установки->Параметры, вкладка Отрисовка -> "Значки в формате SVG")
3. Вызовите менеджер стилей: Настройки->Менеджер стилей.
4. Нажмите кнопку "Импорт".
5. Укажите путь к файлу "all.xml" из данного архива либо нужный из директории by-type/
6. Выберете нужные символы или выделите все и нажмите кнопку "Импорт".

Обратите внимание, что в импортированных символах не должно быть красных кружков.
Если вы видите красные кружки в символах (или не видите некоторых символов, хотя их имена присутствуют в менеджере стилей), 
это означает что пути к SVG иконкам, использованным в данных символах импортированы неправильно. 
Это можно исправить, отредактировав файл "symbology-ng-style.xml", НАХОДЯЩИЙСЯ В ПАПКЕ QGIS ВАШЕГО ПОЛЬЗОВАТЕЛЯ (Linux: ~/.qgis; Windows: users\имя пользователя\.qgis): 
скопируйте нужные пути из файла "all.xml" ИЗ ДАННОГО АРХИВА. 
Например, если нужно исправить условный знак "Виноградники (точечный)_100к", находим соответствующее описание в файле all.xml. Оно будет начинаться с:
    <symbol outputUnit="MM" alpha="1" type="marker" name="Виноградники (точечный)_100к">
Чуть ниже вы увидите строчку:
    <prop k="name" v="/vegetation_grounds/vinary_25k.svg"/>
Скопируйте её и замените соответствующую строчку в файле "symbology-ng-style.xml" 
