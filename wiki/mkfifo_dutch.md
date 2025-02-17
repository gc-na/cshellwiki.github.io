# [Linux] Bash mkfifo gebruik: Maak een named pipe aan

## Overzicht
De `mkfifo` opdracht in Bash wordt gebruikt om een named pipe (of FIFO) aan te maken. Een named pipe is een speciale soort bestand dat wordt gebruikt voor interprocesscommunicatie, waardoor verschillende processen gegevens kunnen uitwisselen.

## Gebruik
De basis syntaxis van de `mkfifo` opdracht is als volgt:

```bash
mkfifo [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-m, --mode`: Hiermee kun je de bestandspermissies instellen voor de aangemaakte pipe.
- `-Z`: Dit is een optie voor SELinux die de context van het bestand instelt.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Een eenvoudige named pipe aanmaken
Om een named pipe met de naam `mijn_pipe` aan te maken, gebruik je de volgende opdracht:

```bash
mkfifo mijn_pipe
```

### Voorbeeld 2: Een named pipe met specifieke permissies aanmaken
Als je een named pipe wilt aanmaken met specifieke permissies, bijvoorbeeld 644, gebruik je:

```bash
mkfifo -m 644 mijn_pipe
```

### Voorbeeld 3: Gegevens naar de pipe schrijven
Je kunt gegevens naar de pipe schrijven met een opdracht zoals:

```bash
echo "Hallo, wereld!" > mijn_pipe
```

### Voorbeeld 4: Gegevens lezen van de pipe
In een andere terminal kun je de gegevens lezen die naar de pipe zijn geschreven:

```bash
cat < mijn_pipe
```

## Tips
- Zorg ervoor dat je de named pipe verwijdert met `rm mijn_pipe` wanneer je deze niet meer nodig hebt, om rommel in je bestandssysteem te voorkomen.
- Named pipes zijn handig voor het synchroniseren van processen; gebruik ze om gegevens tussen verschillende scripts of programma's te delen.
- Test je scripts met `mkfifo` in een veilige omgeving om te begrijpen hoe interprocesscommunicatie werkt voordat je ze in productie gebruikt.