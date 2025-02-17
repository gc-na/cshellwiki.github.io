# [Linux] Bash ss gebruik: Netwerkverbindingen bekijken

## Overzicht
De `ss` (socket statistics) command is een krachtig hulpmiddel in Linux dat wordt gebruikt om netwerkverbindingen en sockets te bekijken. Het biedt gedetailleerde informatie over actieve verbindingen, inclusief TCP, UDP, en andere socket-informatie.

## Gebruik
De basis syntaxis van de `ss` command is als volgt:

```
ss [opties] [argumenten]
```

## Veelvoorkomende opties
- `-t`: Toon alleen TCP-sockets.
- `-u`: Toon alleen UDP-sockets.
- `-l`: Toon alleen luisterende sockets.
- `-p`: Toon de processen die de sockets gebruiken.
- `-n`: Toon IP-adressen en poorten in numerieke vorm in plaats van de hostnamen.

## Veelvoorkomende voorbeelden

### 1. Toon alle actieve verbindingen
```bash
ss
```

### 2. Toon alleen TCP-verbindingen
```bash
ss -t
```

### 3. Toon alleen luisterende sockets
```bash
ss -l
```

### 4. Toon UDP-sockets met procesinformatie
```bash
ss -u -p
```

### 5. Toon verbindingen met numerieke adressen
```bash
ss -n
```

## Tips
- Gebruik de `-s` optie om een samenvatting van socketstatistieken te krijgen.
- Combineer opties voor meer gerichte resultaten, bijvoorbeeld `ss -tunlp` om alle actieve TCP en UDP verbindingen met procesinformatie te tonen.
- Het is handig om `ss` te gebruiken in scripts voor netwerkdiagnose of monitoring.