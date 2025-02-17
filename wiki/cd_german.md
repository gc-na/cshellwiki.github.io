# [Linux] Bash cd Verwendung: Wechseln des Verzeichnisses

## Übersicht
Der `cd`-Befehl (change directory) wird verwendet, um das aktuelle Arbeitsverzeichnis in der Bash-Shell zu ändern. Er ermöglicht es Benutzern, zwischen verschiedenen Verzeichnissen zu navigieren.

## Verwendung
Die grundlegende Syntax des `cd`-Befehls ist:

```bash
cd [Optionen] [Argumente]
```

## Häufige Optionen
- `-`: Wechselt zum vorherigen Verzeichnis.
- `..`: Wechselt zum übergeordneten Verzeichnis.
- `~`: Wechselt zum Home-Verzeichnis des aktuellen Benutzers.

## Häufige Beispiele
- Wechseln in ein spezifisches Verzeichnis:
  ```bash
  cd /pfad/zum/verzeichnis
  ```

- Wechseln zum übergeordneten Verzeichnis:
  ```bash
  cd ..
  ```

- Wechseln zum vorherigen Verzeichnis:
  ```bash
  cd -
  ```

- Wechseln zum Home-Verzeichnis:
  ```bash
  cd ~
  ```

## Tipps
- Verwenden Sie `cd -`, um schnell zwischen zwei Verzeichnissen zu wechseln.
- Nutzen Sie `cd ..` mehrmals, um mehrere Ebenen nach oben zu navigieren (z.B. `cd ../../`).
- Sie können Verzeichnisse mit Tab-Vervollständigung schneller erreichen, indem Sie den Anfangsnamen des Verzeichnisses eingeben und die Tab-Taste drücken.