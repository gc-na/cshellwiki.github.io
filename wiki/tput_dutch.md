# [Linux] Bash tput gebruik: Beheer van terminal eigenschappen

## Overzicht
De `tput`-opdracht wordt gebruikt om terminal eigenschappen te beheren en te manipuleren. Het stelt gebruikers in staat om terminalinstellingen zoals kleuren, cursorpositie en andere weergave-instellingen aan te passen.

## Gebruik
De basis syntaxis van de `tput`-opdracht is als volgt:

```bash
tput [opties] [argumenten]
```

## Veelvoorkomende opties
- `setaf`: Zet de voorgrondkleur.
- `setab`: Zet de achtergrondkleur.
- `clear`: Maakt het terminalvenster schoon.
- `cup`: Verplaatst de cursor naar een specifieke positie.
- `bold`: Zet de tekst in vetgedrukte stijl.

## Veelvoorkomende voorbeelden

### Voorgrondkleur instellen
Om de voorgrondkleur naar rood te veranderen, gebruik je:

```bash
tput setaf 1
```

### Achtergrondkleur instellen
Om de achtergrondkleur naar groen te veranderen, gebruik je:

```bash
tput setab 2
```

### Terminal schoonmaken
Om het terminalvenster schoon te maken, gebruik je:

```bash
tput clear
```

### Cursorpositie instellen
Om de cursor naar rij 10, kolom 20 te verplaatsen, gebruik je:

```bash
tput cup 10 20
```

### Vetgedrukte tekst
Om tekst vetgedrukt weer te geven, gebruik je:

```bash
tput bold
```

## Tips
- Combineer verschillende `tput`-opdrachten om complexe opmaak te creëren.
- Gebruik `tput reset` om alle terminalinstellingen naar de standaardwaarden terug te zetten.
- Controleer de beschikbare kleuren en stijlen door `tput colors` en `tput -T xterm-256color` te gebruiken voor een breed scala aan opties.