# Linux/Unix CLI und Bash-Scripting Übersicht

## CLI vs GUI

### CLI (Command Line Interface)
- **Definition**: Textbasierte Bedienung über Befehle
- **Synonyme**: Terminal, Konsole, Shell, Kommandozeile
- **Ressourcen**: Wenig RAM/CPU, schnell, effizient

### GUI (Graphical User Interface)
- **Definition**: Grafische Bedienung mit Maus und Fenstern
- **Ressourcen**: Mehr RAM/CPU, langsamer, benutzerfreundlicher

## Grundlegende Befehle

- `ls` - Dateien auflisten
- `mkdir` - Ordner erstellen
- `diff` - Dateien vergleichen
- `less` - Datei seitenweise anzeigen
- `tail` - Ende einer Datei anzeigen
- `cat` - Datei komplett anzeigen
- `ip` - Netzwerk-Informationen
- `pwd` - aktueller Pfad
- `date` - Datum/Zeit anzeigen
- `touch` - Datei erstellen

## Automatisierung

### Gut automatisierbar
- Backups
- Logs analysieren
- Systemüberwachung
- Datei-Operationen

### Schlecht automatisierbar
- Kreative Entscheidungen
- Komplexe Problemlösung
- Benutzereingaben

## Case Sensitiv
Linux unterscheidet Groß-/Kleinschreibung: `File.txt` ≠ `file.txt`

## Kommentare in Skripts

```bash
# Das ist ein Kommentar
echo "Hallo" # Kommentar am Zeilenende
```

## Cron/Cronjobs
Zeitgesteuerte Aufgaben:

```bash
# Minute Stunde Tag Monat Wochentag Befehl
0 2 * * * /path/to/script.sh  # Täglich 2:00 Uhr
```

## Dateirechte (RWX)

- **r** = read (4), **w** = write (2), **x** = execute (1)
- `chmod 755 datei` = rwxr-xr-x (Owner: alle Rechte, Gruppe/Andere: lesen+ausführen)
- `chown user:group datei` = Besitzer ändern

## Sicherheitsregeln für Skripts

- Keine Ausführrechte für "Other"
- Skripts nicht in öffentlichen Verzeichnissen
- Keine Passwörter im Klartext
- Minimal notwendige Rechte vergeben

## Design-Techniken

- Flussdiagramme
- Pseudocode
- UML-Diagramme
- Strukturierte Programmierung

## Dokumentation von Skripts

**Gründe**: Wartbarkeit, Verständlichkeit, Fehlersuche, Teamarbeit, Compliance

## Tests

- **Vorbereitung**: Testdaten erstellen, Erwartete Ergebnisse definieren
- **Durchführung**: Unit-Tests, Integrationstests, Fehlerfälle testen

## Dateinamen für Skripts

- Kleinbuchstaben, Zahlen, Bindestrich, Unterstrich
- Endung `.sh` für Bash-Skripts
- Keine Leerzeichen oder Sonderzeichen

## Script-Header

```bash
#!/bin/bash
# Beschreibung: Was macht das Skript
# Autor: Name
# Datum: YYYY-MM-DD
# Version: 1.0
```

## Shebang für Bash

```bash
#!/bin/bash
```

## Dateien suchen

```bash
find /pfad -name "dateiname"
locate dateiname
```

## Ausgaben umleiten/unterdrücken

```bash
befehl > /dev/null 2>&1  # Alles unterdrücken
befehl 2> fehler.log     # Fehler in Datei
```

## Textsuche in Dateien

```bash
grep "suchstring" datei.txt
grep -r "suchstring" /verzeichnis/
```

## Wildcards

- `*` = beliebige Zeichen
- `?` = ein Zeichen
- `[abc]` = a, b oder c
- `[a-z]` = Buchstaben a bis z

## Parameter in Skripts

```bash
$1, $2, $3  # Erste, zweite, dritte Parameter
$0          # Skriptname
$#          # Anzahl Parameter
$@          # Alle Parameter
```

## Ausgaben umleiten

```bash
befehl > datei.txt      # Ausgabe in Datei
befehl >> datei.txt     # Ausgabe anhängen
befehl | other_befehl   # Pipe zu anderem Befehl
```

## SSH/SCP Dateien übertragen

```bash
scp datei.txt user@server:/pfad/     # Datei kopieren
ssh user@server "befehl"             # Remote-Befehl
```

## Arrays in Bash

```bash
array=("wert1" "wert2" "wert3")
echo ${array[0]}  # Erstes Element
echo ${array[@]}  # Alle Elemente
```

## Schleifen

### For-Schleife
```bash
for i in 1 2 3; do
    echo $i
done
```

### While-Schleife
```bash
while [ $i -lt 10 ]; do
    echo $i
    i=$((i+1))
done
```

## Dateisystem navigieren

```bash
cd /pfad        # Verzeichnis wechseln
nano datei.txt  # Datei bearbeiten
touch datei.txt # Datei erstellen
rm datei.txt    # Datei löschen
```

## Bash-Skript erstellen und ausführen

```bash
nano mein_script.sh    # Skript erstellen
chmod +x mein_script.sh # Ausführbar machen
./mein_script.sh       # Ausführen
```


## Skript bearbeiten
```bash
:w         # Skript speichern
:q!        # Vim verlassen
vim filename # vim starten
```
