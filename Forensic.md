## Hex-редакторы
- `xxd [filename]`
- `hexeditor [filename]`
- `hexyl [filename]` (не редактор, а прикольный вьювер)
- Онлайн вариант - [`hexed.it`](https://hexed.it/) 

## Утилитки для стеги

### \[LW] binwalk
- `binwalk [filename]` -> 
считывает все сигнатуры файла и обнаруживает скрытые в нём друуугииие файлы.
- `binwalk -e [filename]` ->
извлекает всё, что внутри файла
- `binwalk --dd='.*' [filename]` ->
если сломалось и не вытаскивает ничего (да, Sp1av, спасибо, что подсказал<3)
Также оно умеет сканировать данные с дизассемблированием и сравнивать бинарные данные. [Подробнее о binwalk](https://kali.tools/?p=6771) 

### \[L-] exiftool
`exiftool [filename]` -> смотрит метаданные файла
Также умеет записывать свои теги в матаданные и управлять ими. Для винды есть аналоги и онлайн версии. [Подробнее о exiftool](https://kali.tools/?p=5984)
### \[L-] zsteg
`zsteg [filename]` ->
анализирует чуть ли не всё, что может быть в файле, в т.ч цветовые каналы (по одному) на наличие чего-то скрытого. [Подробнее о zsteg](https://github.com/zed-0xff/zsteg)

### \[LW] stegsolve
- есть GUI
- ОНО ТЕБЯ СОЖРЁТ!
- [Установка и примеры использования](https://kmb.cybber.ru/stego/stegsolve/main.html)
Умеет почти всё, что можно себе представить.. xor картинки на картинку, анализ по цветовым каналам, извлечение данных из изображения миллиардом способов

### \[LW] sigBits
- очень хочет либу `Pillow` для работы:
`pip install Pillow`
- Скачиваем с гита `.py` файлик и запускаем с флагами:
`python sigBits.py -t=lsb -o=rgb -out=[output file] -e=row [filename]`
Анализирует  картинки по пикселям на наличие вшитой записи (мой годовой проект) по всем цветовым каналам. Про флаги и опции на гитхабе. [Подробнее о sigBits](https://github.com/Pulho/sigBits)

### \[-W] GraphBitStreamer (GBS)
- есть GUI
-  вкусняшка для .raw файликов (картиночек особенно) - визуализирует сырые байты как пиксели картинки
На гите лежит .exe, вспринципе достаточно просто тыкать ползунки, долго и усердно. [Подробнее о GSB]()


##

### AUDACITY
Прога для смотрения музики

### Autopsy
Прога для анализа образа диска

### Volatility 
Да поможет тебе Бог. (и HackTricks)
- `volatility -h` 
- `volatility imageinfo -f file.dmp` -> покажет инфу про образ
- `volatility -f file.dmp --profile=Win7SP1x64 hivelist` -> инфа о юзерах
- `volatility -f file.dmp --profile=Win7SP1x64 hashdump` -> хэши глупых паролей
- `volatility -f file.dmp --profile=Win7SP1x64 clipboard` -> буфер глупого обмена
