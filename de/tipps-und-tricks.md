## Tipps und Tricks
### Entfernen der Infoboxen beim Beitreten
Bei jedem Beitreten eines Servers werden die Serverinfo und das Map Briefing angezeigt. Damit beim Testen Zeit gespart wird, sollten diese Nachrichten entfernt werden.

Lösche die Datei `sys/serverinfo.txt`, um die Serverinfo zu entfernen.

Lösche alle Textdateien im Ordner `maps`, um die Map Briefings zu entfernen.

Infos löschen:
```bash
rm sys/serverinfo.txt
rm maps/*.txt
```

#### Deaktivieren / Aktivieren der Infoboxen
Alternativ können die Dateien umbenannt oder verschoben werden.

Infos deaktivieren:
```bash
mv sys/serverinfo.txt sys/serverinfo.inactive.txt
mkdir maps/briefings
mv maps/*.txt maps/briefings
```

Infos reaktivieren:
```bash
mv sys/serverinfo.inactive.txt sys/serverinfo.txt
mv maps/*.txt maps/briefings
rmdir maps/briefings
```

### Lua Skripts validieren
Um Syntaxfehler direkt in der Entwicklung zu bemerken, kann der offizielle Lua-Compiler verwendet werden.

Solltest du Atom verwenden, hilft dir das Paket `linter-lua`. Installiere dies über die Einstellungen oder den Befehl `apm install linter-lua`.
