# [Linux] Bash crontab Bruk: Planlegg og kjør oppgaver automatisk

## Oversikt
`crontab`-kommandoen brukes til å planlegge og administrere tidsbestemte oppgaver i Unix-lignende operativsystemer. Den lar brukere spesifisere kommandoer som skal kjøres på bestemte tidspunkter eller intervaller, noe som er nyttig for automatisering av vedlikeholdsoppgaver og andre rutinejobber.

## Bruk
Grunnleggende syntaks for `crontab`-kommandoen er som følger:

```bash
crontab [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e`: Rediger den nåværende crontab-filen for brukeren.
- `-l`: List opp den nåværende crontab-filen for brukeren.
- `-r`: Slett den nåværende crontab-filen for brukeren.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `crontab` kan brukes:

### Eksempel 1: Kjør et skript hver dag kl. 2:00
```bash
0 2 * * * /path/to/script.sh
```

### Eksempel 2: Kjør en kommando hvert 15. minutt
```bash
*/15 * * * * /path/to/command
```

### Eksempel 3: Sjekk systemstatus hver mandag kl. 8:30
```bash
30 8 * * 1 /path/to/status_check.sh
```

### Eksempel 4: Rens opp midlertidige filer hver søndag kl. 23:00
```bash
0 23 * * 0 /path/to/cleanup.sh
```

## Tips
- Bruk `crontab -l` for å se hvilke oppgaver du allerede har planlagt.
- Husk å bruke full sti til skriptene eller kommandoene du ønsker å kjøre for å unngå problemer med arbeidskatalogen.
- Test skriptene dine manuelt før du legger dem til i crontab for å sikre at de fungerer som forventet.