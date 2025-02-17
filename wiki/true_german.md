# [Linux] Bash true Verwendung: Gibt immer den Status 0 zurück

## Übersicht
Der `true` Befehl in Bash ist ein einfacher Befehl, der immer den Status 0 zurückgibt, was bedeutet, dass er erfolgreich ausgeführt wurde. Er wird häufig in Skripten verwendet, um Platzhalter für erfolgreiche Bedingungen zu schaffen oder um Bedingungen zu simulieren.

## Verwendung
Die grundlegende Syntax des `true` Befehls ist sehr einfach:

```bash
true [Optionen] [Argumente]
```

In der Regel wird `true` ohne Optionen oder Argumente verwendet.

## Häufige Optionen
Der `true` Befehl hat keine spezifischen Optionen oder Argumente, die üblicherweise verwendet werden. Er ist darauf ausgelegt, einfach und direkt zu sein.

## Häufige Beispiele

### Beispiel 1: Einfache Verwendung
Ein einfaches Beispiel, um den Befehl `true` auszuführen:

```bash
true
```

### Beispiel 2: Verwendung in einer Bedingung
`true` kann in einer if-Anweisung verwendet werden, um immer den "wahren" Zweig auszuführen:

```bash
if true; then
    echo "Dieser Block wird immer ausgeführt."
fi
```

### Beispiel 3: Schleifensteuerung
`true` kann auch in Schleifen verwendet werden, um eine unendliche Schleife zu erzeugen:

```bash
while true; do
    echo "Diese Schleife läuft unendlich."
    sleep 1
done
```

## Tipps
- Verwenden Sie `true`, um Platzhalter für Bedingungen in Skripten zu schaffen, wenn Sie sicherstellen möchten, dass ein Block immer ausgeführt wird.
- Kombinieren Sie `true` mit anderen Befehlen in Pipelines, um die Ausführung zu steuern, ohne dass ein Fehlerstatus zurückgegeben wird.
- Nutzen Sie `true` in Testszenarien, um sicherzustellen, dass der Code auch bei unerwarteten Bedingungen weiterhin funktioniert.