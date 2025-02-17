# [Linux] Bash bindkey gebruik: Toewijzen van toetsen aan functies

## Overzicht
De `bindkey` opdracht in Bash wordt gebruikt om toetsenbordtoetsen te koppelen aan specifieke functies of commando's in de shell. Dit kan handig zijn voor het aanpassen van je omgeving en het versnellen van je workflow.

## Gebruik
De basis syntaxis van de `bindkey` opdracht is als volgt:

```bash
bindkey [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-e`: Schakelt over naar de Emacs-toetsenbindingen.
- `-v`: Schakelt over naar de Vi-toetsenbindingen.
- `-s`: Koppelt een toets aan een reeks commando's.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Toetsenbinding voor het wissen van de regel
Om de toets `Ctrl + W` te koppelen aan het wissen van de huidige regel, gebruik je:

```bash
bindkey '^W' backward-kill-line
```

### Voorbeeld 2: Toetsenbinding voor het uitvoeren van een specifiek commando
Als je de toets `F5` wilt gebruiken om een script uit te voeren, kun je dit doen:

```bash
bindkey -s '^[15~' 'bash /pad/naar/script.sh\n'
```

### Voorbeeld 3: Schakelen tussen Emacs en Vi modus
Om over te schakelen naar de Emacs modus, gebruik je:

```bash
bindkey -e
```

## Tips
- Experimenteer met verschillende toetsenbindingen om je workflow te optimaliseren.
- Documenteer je toetsenbindingen, zodat je ze later gemakkelijk kunt terugvinden of delen.
- Gebruik de `bindkey -L` opdracht om een lijst van huidige toetsenbindingen te bekijken.