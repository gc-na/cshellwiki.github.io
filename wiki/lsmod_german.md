# [Linux] Bash lsmod Verwendung: Zeigt geladene Kernel-Module an

## Übersicht
Der Befehl `lsmod` wird verwendet, um eine Liste der derzeit geladenen Kernel-Module in einem Linux-System anzuzeigen. Diese Module sind Treiber oder andere Programme, die vom Kernel zur Unterstützung von Hardware oder zur Bereitstellung von Funktionen verwendet werden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
lsmod [Optionen] [Argumente]
```

## Häufige Optionen
- **-h, --help**: Zeigt eine Hilfemeldung mit den verfügbaren Optionen an.
- **-n, --noheadings**: Unterdrückt die Kopfzeilen in der Ausgabe.
- **-o, --output**: Ermöglicht die Angabe von spezifischen Ausgabefeldern.

## Häufige Beispiele
- Um alle geladenen Module anzuzeigen:

```bash
lsmod
```

- Um die Ausgabe ohne Kopfzeilen zu erhalten:

```bash
lsmod -n
```

- Um spezifische Ausgabefelder anzuzeigen, z.B. nur die Modulnamen:

```bash
lsmod --output=name
```

## Tipps
- Verwenden Sie `lsmod` in Kombination mit `grep`, um nach einem bestimmten Modul zu suchen, z.B.:

```bash
lsmod | grep <Modulname>
```

- Beachten Sie, dass `lsmod` keine Optionen zum Laden oder Entladen von Modulen bietet; dafür sollten Sie `modprobe` oder `rmmod` verwenden.
- Überprüfen Sie regelmäßig die geladenen Module, um sicherzustellen, dass alle benötigten Treiber aktiv sind und keine unnötigen Module geladen sind.