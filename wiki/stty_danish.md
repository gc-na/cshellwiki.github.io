# [Linux] Bash stty brug: Juster terminalindstillinger

## Oversigt
`stty` er et Bash-kommando, der bruges til at ændre og vise terminalens indstillinger. Det giver brugeren mulighed for at konfigurere, hvordan terminalen håndterer input og output, hvilket kan være nyttigt for at forbedre brugeroplevelsen eller tilpasse terminalens adfærd.

## Brug
Den grundlæggende syntaks for `stty`-kommandoen er:

```bash
stty [options] [arguments]
```

## Almindelige muligheder
- `-a`: Viser alle terminalindstillinger.
- `-g`: Gemmer terminalindstillingerne i en form, der kan bruges med `stty`.
- `erase`: Angiver tegn, der skal bruges til at slette den sidste indtastede karakter.
- `kill`: Angiver tegn, der skal bruges til at slette hele linjen.
- `intr`: Angiver tegn, der bruges til at afbryde en kørende proces.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `stty` kan bruges:

### 1. Vis alle terminalindstillinger
For at se alle indstillinger for din terminal kan du bruge:

```bash
stty -a
```

### 2. Ændre sletningstegnet
Hvis du vil ændre sletningstegnet til `Ctrl+D`, kan du gøre det med:

```bash
stty erase ^D
```

### 3. Gem terminalindstillinger
For at gemme de nuværende terminalindstillinger til senere brug, kan du køre:

```bash
stty -g > terminal_settings.txt
```

### 4. Gendan terminalindstillinger
For at gendanne terminalindstillinger fra en gemt fil, kan du bruge:

```bash
stty $(cat terminal_settings.txt)
```

## Tips
- Vær forsigtig, når du ændrer terminalindstillinger, da forkert konfiguration kan gøre terminalen svær at bruge.
- Brug `stty -a` regelmæssigt for at holde styr på dine nuværende indstillinger.
- Hvis du arbejder med scripts, kan det være nyttigt at gemme og gendanne terminalindstillinger for at sikre, at scriptet ikke forstyrrer brugerens miljø.