# [Linux] Bash exec gebruik: Voer een commando uit in de huidige shell

## Overzicht
De `exec` opdracht in Bash wordt gebruikt om een commando uit te voeren en de huidige shell te vervangen door dat commando. Dit betekent dat na het uitvoeren van het commando, de oorspronkelijke shell niet meer beschikbaar is. Het is handig voor situaties waarin je een programma wilt uitvoeren zonder een nieuwe shell te openen.

## Gebruik
De basis syntaxis van de `exec` opdracht is als volgt:

```bash
exec [opties] [commando] [argumenten]
```

## Veelvoorkomende Opties
- `-a` : Hiermee kan je een andere naam voor het commando opgeven.
- `-l` : Start het commando als een login-shell.
- `-p` : Voorkomt dat de omgevingsvariabelen van de huidige shell worden doorgegeven aan het nieuwe commando.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Vervang de huidige shell met een ander commando
```bash
exec /bin/bash
```
Dit vervangt de huidige shell door een nieuwe Bash-shell.

### Voorbeeld 2: Voer een script uit en vervang de shell
```bash
exec ./myscript.sh
```
Hiermee wordt `myscript.sh` uitgevoerd en de huidige shell wordt vervangen door het script.

### Voorbeeld 3: Gebruik exec met een andere naam
```bash
exec -a mycustomname /bin/ls
```
Dit voert de `ls` opdracht uit, maar het zal verschijnen als `mycustomname` in de processenlijst.

## Tips
- Gebruik `exec` wanneer je wilt dat een script of programma de controle overneemt zonder een nieuwe shell te openen.
- Wees voorzichtig met `exec`, omdat het de huidige shell vervangt en je niet meer terug kunt keren naar de oorspronkelijke shell.
- Test je commando's in een veilige omgeving voordat je ze in een productieomgeving uitvoert, vooral als je `exec` gebruikt om kritieke scripts uit te voeren.