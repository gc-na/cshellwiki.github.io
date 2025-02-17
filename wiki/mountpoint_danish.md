# [Linux] Bash mountpoint brug: Kontrollerer om et bibliotek er et mountpoint

## Overview
`mountpoint` er et Bash-kommando, der bruges til at kontrollere, om et givet bibliotek fungerer som et mountpoint for et filsystem. Det er nyttigt til at verificere, om et bestemt sted i filsystemet er blevet monteret korrekt.

## Usage
Den grundlæggende syntaks for `mountpoint`-kommandoen er:

```bash
mountpoint [options] [arguments]
```

## Common Options
- `-q`: Kører i stille tilstand, uden at udskrive nogen output, men returnerer en exit-status.
- `-d`: Udskriver en besked, hvis det angivne argument ikke er et mountpoint.
- `--help`: Viser hjælp og en liste over tilgængelige muligheder.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du bruger `mountpoint`:

1. **Kontroller et mountpoint**:
   For at kontrollere, om `/mnt/data` er et mountpoint, kan du bruge følgende kommando:
   ```bash
   mountpoint /mnt/data
   ```

2. **Brug af stille tilstand**:
   Hvis du kun vil have exit-statussen uden output, kan du køre:
   ```bash
   mountpoint -q /mnt/data
   ```

3. **Kontroller flere mountpoints**:
   Du kan også kontrollere flere mountpoints på én gang:
   ```bash
   mountpoint /mnt/data /mnt/backup
   ```

4. **Brug af -d option**:
   For at få en besked, hvis et argument ikke er et mountpoint:
   ```bash
   mountpoint -d /mnt/invalid
   ```

## Tips
- Brug `mountpoint -q` i scripts, hvor du kun har brug for at vide, om et mountpoint eksisterer, uden at generere output.
- Tjek altid mountpoints, før du forsøger at tilgå data, for at undgå fejl.
- Kombiner `mountpoint` med andre kommandoer i scripts for at sikre, at nødvendige filsystemer er tilgængelige, før du udfører operationer.