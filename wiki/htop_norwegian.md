# [Linux] Bash htop bruk: Vise systemprosessene i sanntid

## Oversikt
htop er et interaktivt prosessvisningsverktøy for Unix-lignende systemer. Det gir en dynamisk visning av systemprosesser, minnebruk og CPU-bruk, og lar brukeren enkelt overvåke og administrere prosesser.

## Bruk
Den grunnleggende syntaksen for htop-kommandoen er:

```bash
htop [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h`, `--help`: Viser hjelpeteksten for htop.
- `-s`, `--sort`: Sorterer prosessene etter en spesifisert kolonne.
- `-p`, `--pid`: Viser bare prosessene med de angitte prosidene.
- `-u`, `--user`: Viser bare prosessene til den angitte brukeren.

## Vanlige eksempler
For å starte htop, kan du ganske enkelt skrive:

```bash
htop
```

For å vise prosessene til en spesifikk bruker:

```bash
htop -u brukernavn
```

For å sortere prosessene etter minnebruk:

```bash
htop -s MEM
```

For å vise prosessene med spesifikke PID-er:

```bash
htop -p 1234,5678
```

## Tips
- Bruk piltastene for å navigere mellom prosessene.
- Trykk `F9` for å avslutte en prosess, og velg deretter signalet du ønsker å sende.
- Du kan bruke `F6` for å endre sorteringskriteriene mens htop kjører.
- For en mer detaljert visning, kan du trykke `F1` for å få tilgang til hjelpen direkte fra htop-grensesnittet.