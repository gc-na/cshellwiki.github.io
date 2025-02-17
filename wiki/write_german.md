# [Linux] Bash write Verwendung: Nachrichten an andere Benutzer senden

## Übersicht
Der `write` Befehl in Bash ermöglicht es Benutzern, Nachrichten direkt an andere Benutzer auf demselben System zu senden. Dies ist besonders nützlich in Mehrbenutzerumgebungen, wo schnelle Kommunikation erforderlich ist.

## Verwendung
Die grundlegende Syntax des `write` Befehls lautet:

```bash
write [Benutzername] [Terminal]
```

Wenn kein Terminal angegeben wird, wird standardmäßig das Terminal des angegebenen Benutzers verwendet.

## Häufige Optionen
- `-n`: Verhindert, dass der Benutzer benachrichtigt wird, wenn eine Nachricht gesendet wird.
- `-h`: Zeigt eine Hilfe-Information an.

## Häufige Beispiele
1. **Nachricht an einen Benutzer senden:**
   Um eine Nachricht an den Benutzer `max` zu senden, geben Sie einfach ein:
   ```bash
   write max
   ```
   Danach können Sie Ihre Nachricht eingeben und mit `Strg+D` beenden.

2. **Nachricht an einen bestimmten Terminal senden:**
   Wenn Sie wissen, dass `max` auf `pts/1` eingeloggt ist, können Sie die Nachricht direkt dorthin senden:
   ```bash
   write max pts/1
   ```

3. **Nachricht ohne Benachrichtigung senden:**
   Um eine Nachricht zu senden, ohne dass der Empfänger benachrichtigt wird:
   ```bash
   write -n max
   ```

## Tipps
- Stellen Sie sicher, dass der Empfänger nicht den `mesg n` Befehl ausgeführt hat, da dies das Empfangen von Nachrichten blockiert.
- Nutzen Sie `write` in Kombination mit `who`, um herauszufinden, wer gerade eingeloggt ist und auf welchem Terminal sie sich befinden.
- Seien Sie höflich und verwenden Sie `write` für wichtige Mitteilungen, um den Empfänger nicht unnötig zu stören.