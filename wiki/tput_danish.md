# [Linux] Bash tput brug: Kontroller terminalens udseende

## Oversigt
`tput` er et Bash-kommando, der bruges til at interagere med terminalens kapabiliteter. Det giver brugeren mulighed for at ændre terminalens udseende og adfærd, såsom at ændre tekstfarver, flytte markøren og rydde skærmen.

## Brug
Den grundlæggende syntaks for `tput`-kommandoen er:

```bash
tput [muligheder] [argumenter]
```

## Almindelige muligheder
- `setaf [farve]`: Sætter tekstfarven til den angivne farve.
- `setab [farve]`: Sætter baggrundsfarven til den angivne farve.
- `clear`: Rydder terminalskærmen.
- `cup [række] [kolonne]`: Flytter markøren til den angivne række og kolonne.
- `bold`: Gør teksten fed.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `tput`:

### Ændre tekstfarve
For at ændre tekstfarven til rød, kan du bruge:

```bash
tput setaf 1
echo "Denne tekst er rød"
tput sgr0  # Nulstil farverne
```

### Ændre baggrundsfarve
For at ændre baggrundsfarven til grøn, kan du bruge:

```bash
tput setab 2
echo "Denne tekst har en grøn baggrund"
tput sgr0  # Nulstil farverne
```

### Rydde skærmen
For at rydde terminalskærmen, kan du bruge:

```bash
tput clear
```

### Flytte markøren
For at flytte markøren til række 5 og kolonne 10, kan du bruge:

```bash
tput cup 5 10
echo "Markøren er flyttet her"
```

### Gøre teksten fed
For at gøre teksten fed, kan du bruge:

```bash
tput bold
echo "Denne tekst er fed"
tput sgr0  # Nulstil til normal
```

## Tips
- Husk altid at nulstille terminalens indstillinger med `tput sgr0` efter at have ændret farver eller stilarter for at undgå uventede resultater.
- Du kan finde ud af, hvilke farver der er tilgængelige, ved at eksperimentere med `tput setaf` og `tput setab` med forskellige tal (0-7 for standardfarver).
- `tput` kan være nyttigt i scripts til at forbedre brugeroplevelsen ved at gøre output mere visuelt tiltalende.