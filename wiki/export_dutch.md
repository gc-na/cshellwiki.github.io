# [Linux] Bash export gebruik: Omgevingsvariabelen instellen

## Overzicht
De `export` opdracht in Bash wordt gebruikt om omgevingsvariabelen in te stellen en beschikbaar te maken voor sub-processen. Dit is nuttig wanneer je variabelen wilt delen met andere programma's of scripts die je uitvoert vanuit de huidige shell.

## Gebruik
De basis syntaxis van de `export` opdracht is als volgt:

```bash
export [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n`: Verwijdert de exportstatus van een variabele, waardoor deze niet meer beschikbaar is voor sub-processen.
- `-p`: Toont een lijst van alle geëxporteerde variabelen en hun waarden.

## Veelvoorkomende Voorbeelden

### 1. Een nieuwe omgevingsvariabele instellen
```bash
export MY_VAR="Hallo Wereld"
```

### 2. Een omgevingsvariabele controleren
```bash
echo $MY_VAR
```

### 3. Een omgevingsvariabele verwijderen
```bash
export -n MY_VAR
```

### 4. Een variabele exporteren en direct gebruiken
```bash
export PATH="$PATH:/usr/local/bin"
```

### 5. Lijst van geëxporteerde variabelen weergeven
```bash
export -p
```

## Tips
- Zorg ervoor dat je de juiste syntaxis gebruikt bij het instellen van variabelen om fouten te voorkomen.
- Gebruik `export` in je `.bashrc` of `.bash_profile` om omgevingsvariabelen automatisch in te stellen bij het opstarten van een nieuwe shell.
- Controleer altijd de waarde van een variabele met `echo` voordat je deze in scripts gebruikt, om te bevestigen dat deze correct is ingesteld.