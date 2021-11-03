# LCD

| Befehl | Beschreibung |
|---|---|
| `lcd_i2c_t lcd = {0};` | Vorinitialisieren der Variable |
| `int8_t opt_address = 0x27;<br>lcd_i2c_setup(&lcd, opt_address);` | Initalisierung des LCD Displays<br> Rückgabewert -1, beim Auftritt von Fehlern |
| `lcd_i2c_init(&lcd);` |  |
| `lcd.rows = 2;<br>lcd.cols = 16;` | Sitzen der LCD Dimension |
| `lcd_i2c_backlight(&lcd, 1);` | LCD Hintergrundslicht einschalten |
| `char formatedText[30];<br>sprintf(formatedText, "Temp: %.2f °C", temperature);` | Ausgabe vorbereiten mit sprintf |
| `lcd_i2c_gotoxy(&lcd, 0, 0);` | Displaycursor setzen |
| `lcd_i2c_puts(&lcd, formatedText);` | Schreiben des vorbereiteten Textes auf das LCD Display |
