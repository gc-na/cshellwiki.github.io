# [Linux] C Shell (csh) popd Verwendung: Wechselt das Verzeichnis zurück

## Übersicht
Der Befehl `popd` wird in der C Shell verwendet, um das zuletzt gespeicherte Verzeichnis von der Verzeichnisstapel zu entfernen und in dieses Verzeichnis zu wechseln. Dies ist besonders nützlich, wenn Sie zwischen mehreren Verzeichnissen navigieren und den Überblick über Ihren Standort behalten möchten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
popd [options] [arguments]
```

## Häufige Optionen
- **`-n`**: Zeigt das neue Verzeichnis an, wechselt jedoch nicht dorthin.
- **`+n`**: Wechselt zum n-ten Verzeichnis im Stapel, wobei `n` die Position im Stapel angibt.
- **`-n`**: Wechselt zum n-ten Verzeichnis von hinten im Stapel.

## Häufige Beispiele

1. **Zurückwechseln zum vorherigen Verzeichnis:**
   ```csh
   popd
   ```

2. **Wechseln zum zweiten Verzeichnis im Stapel:**
   ```csh
   popd +1
   ```

3. **Wechseln zum ersten Verzeichnis von hinten:**
   ```csh
   popd -1
   ```

4. **Verzeichnis anzeigen, ohne zu wechseln:**
   ```csh
   popd -n
   ```

## Tipps
- Stellen Sie sicher, dass Sie zuvor mit `pushd` ein Verzeichnis auf den Stapel gelegt haben, bevor Sie `popd` verwenden.
- Nutzen Sie `dirs`, um den aktuellen Verzeichnisstapel anzuzeigen, bevor Sie `popd` ausführen.
- Verwenden Sie `popd` in Kombination mit `pushd`, um effizient zwischen mehreren Verzeichnissen zu navigieren.