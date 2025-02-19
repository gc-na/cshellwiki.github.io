# [Linux] C Shell (csh) id Verwendung: Benutzeridentifikation anzeigen

## Übersicht
Der Befehl `id` wird verwendet, um Informationen über den aktuellen Benutzer und dessen Gruppenmitgliedschaften anzuzeigen. Dies umfasst die Benutzer-ID (UID), die Gruppen-ID (GID) und die Gruppen, denen der Benutzer angehört.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
id [Optionen] [Argumente]
```

## Häufige Optionen
- `-u`: Zeigt nur die Benutzer-ID (UID) an.
- `-g`: Zeigt nur die Gruppen-ID (GID) an.
- `-G`: Listet alle Gruppen-IDs auf, denen der Benutzer angehört.
- `-n`: Gibt die Namen anstelle der IDs aus.

## Häufige Beispiele
Um die Benutzer- und Gruppeninformationen des aktuellen Benutzers anzuzeigen, verwenden Sie:

```csh
id
```

Um nur die Benutzer-ID anzuzeigen, verwenden Sie:

```csh
id -u
```

Um nur die Gruppen-ID anzuzeigen, verwenden Sie:

```csh
id -g
```

Um alle Gruppen-IDs des Benutzers anzuzeigen, verwenden Sie:

```csh
id -G
```

Um die Benutzer- und Gruppeninformationen eines bestimmten Benutzers (z. B. `username`) anzuzeigen, verwenden Sie:

```csh
id username
```

## Tipps
- Verwenden Sie die Option `-n`, um die Ausgabe benutzerfreundlicher zu gestalten, indem Sie die Namen anstelle der IDs anzeigen.
- Kombinieren Sie Optionen, um spezifischere Informationen zu erhalten, z. B. `id -Gn`, um die Gruppennamen anzuzeigen.
- Nutzen Sie `man id`, um die vollständige Dokumentation und weitere Optionen zu lesen.