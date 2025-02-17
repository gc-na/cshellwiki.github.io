# [Linux] Bash 7z Verwendung: Dateien komprimieren und dekomprimieren

## Übersicht
Der `7z` Befehl ist ein leistungsstarkes Tool zur Dateikompression und -dekompression. Es unterstützt verschiedene Archive-Formate und bietet eine hohe Kompressionsrate.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
7z [Optionen] [Argumente]
```

## Häufige Optionen
- `a`: Fügt Dateien zu einem Archiv hinzu.
- `x`: Entpackt ein Archiv.
- `l`: Listet den Inhalt eines Archivs auf.
- `d`: Löscht Dateien aus einem Archiv.
- `t`: Überprüft die Integrität eines Archivs.

## Häufige Beispiele

### 1. Ein Archiv erstellen
Um ein neues Archiv zu erstellen und Dateien hinzuzufügen, verwenden Sie:

```bash
7z a archiv.7z datei1.txt datei2.txt
```

### 2. Ein Archiv entpacken
Um ein Archiv zu entpacken, verwenden Sie:

```bash
7z x archiv.7z
```

### 3. Den Inhalt eines Archivs auflisten
Um die Dateien in einem Archiv anzuzeigen, verwenden Sie:

```bash
7z l archiv.7z
```

### 4. Dateien aus einem Archiv löschen
Um eine Datei aus einem Archiv zu entfernen, verwenden Sie:

```bash
7z d archiv.7z datei1.txt
```

### 5. Die Integrität eines Archivs überprüfen
Um die Integrität eines Archivs zu überprüfen, verwenden Sie:

```bash
7z t archiv.7z
```

## Tipps
- Verwenden Sie die Option `-p`, um ein Passwort für Ihr Archiv festzulegen, z.B. `7z a -pMeinPasswort archiv.7z datei.txt`.
- Nutzen Sie die Option `-m0=lzma2` für eine bessere Kompression, wenn die Geschwindigkeit nicht entscheidend ist.
- Achten Sie darauf, die Dateiendungen korrekt zu verwenden, um Komplikationen beim Entpacken zu vermeiden.