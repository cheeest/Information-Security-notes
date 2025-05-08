## Hex-редакторы
- `xxd [filename]`
- `hexeditor [filename]`
- Онлайн вариант - [`hexed.it`](https://hexed.it/) 

## Утилитки для стеги

### binwalk
- `binwalk [filename]` -> 
считывает все сигнатуры файла и обнаруживает скрытые в нём друуугииие файлы.
- `binwalk -e [filename]` ->
извлекает всё, что внутри файла
- `binwalk --dd='.*' [filename]` ->
если сломалось и не вытаскивает ничего (да, Sp1av, спасибо, что подсказал<3)
Также оно умеет сканировать данные с дизассемблированием и сравнивать бинарные данные. [Подробнее о binwalk](https://kali.tools/?p=6771) 

### exiftool
`exiftool [filename]` -> смотрит метаданные файла
Также умеет записывать свои теги в матаданные и управлять ими. [Подробнее о exiftool](https://kali.tools/?p=5984)
### zsteg
`zsteg [filename]` ->
анализирует чуть ли не всё, что может быть в файле, в т.ч цветовые каналы (по одному) на наличие чего-то скрытого. [Подробнее о zsteg](https://github.com/zed-0xff/zsteg)

### stegsolve
- есть GUI
- ОНО ТЕБЯ СОЖРЁТ!
- [Установка и примеры использования](https://kmb.cybber.ru/stego/stegsolve/main.html)
Умеет почти всё, что можно себе представить.. xor картинки на картинку, анализ по цветовым каналам, извлечение данных из изображения миллиардом способов

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
