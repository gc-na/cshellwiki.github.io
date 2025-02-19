# [Linux] C Shell (csh) lsmod Verwendung: Zeigt geladene Kernel-Module an

## Übersicht
Der Befehl `lsmod` wird verwendet, um eine Liste der derzeit geladenen Kernel-Module in einem Linux-System anzuzeigen. Dies ist nützlich, um zu überprüfen, welche Module aktiv sind und welche möglicherweise geladen oder entladen werden müssen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
lsmod [optionen] [argumente]
```

## Häufige Optionen
- `-h`, `--help`: Zeigt eine Hilfe-Seite mit Informationen zur Verwendung des Befehls an.
- `-n`, `--no-heading`: Unterdrückt die Kopfzeile in der Ausgabe.

## Häufige Beispiele
Um alle geladenen Module anzuzeigen, verwenden Sie einfach:

```csh
lsmod
```

Um die Ausgabe ohne Kopfzeile zu erhalten, verwenden Sie:

```csh
lsmod -n
```

Um Hilfe zum Befehl anzuzeigen, verwenden Sie:

```csh
lsmod --help
```

## Tipps
- Überprüfen Sie regelmäßig die geladenen Module, um sicherzustellen, dass keine unerwünschten Module aktiv sind.
- Nutzen Sie `grep`, um gezielt nach einem bestimmten Modul zu suchen, z.B.:

```csh
lsmod | grep modulname
```

- Denken Sie daran, dass Änderungen an geladenen Modulen möglicherweise einen Neustart des Systems erfordern, um wirksam zu werden.