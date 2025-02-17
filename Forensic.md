### xxd
`xxd [filename]` -> hexdump файла

### binwalk
`binwalk [filename]` -> считывает все сигнатуры файла и обнаруживает скрытые в нём друуугииие файлы. Флаг `-e` извлекает их

### exiftool
`exiftool [filename]` -> смотрит метадату файла

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
