# [Linux] Bash logrotate brug: Håndtering af logfiler

## Oversigt
`logrotate` er et værktøj til automatisk håndtering af logfiler på Linux-systemer. Det bruges til at rotere, komprimere og slette logfiler for at forhindre, at de fylder for meget og for at holde systemet organiseret.

## Brug
Den grundlæggende syntaks for `logrotate` er:

```bash
logrotate [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f`: Tvinger rotation af logfiler, selvom det ikke er nødvendigt.
- `-s`: Angiver en specifik statusfil, der bruges til at spore rotationens tilstand.
- `-v`: Aktivér detaljeret uddata, så du kan se, hvad der sker under rotationen.
- `-d`: Kør i "dry run" tilstand, hvilket betyder, at ingen ændringer foretages, men du kan se, hvad der ville ske.

## Almindelige eksempler

### 1. Grundlæggende rotation
For at rotere logfilerne i henhold til standardkonfigurationen:

```bash
logrotate /etc/logrotate.conf
```

### 2. Tving rotation
For at tvinge rotation af logfilerne, selvom det ikke er nødvendigt:

```bash
logrotate -f /etc/logrotate.conf
```

### 3. Detaljeret uddata
For at få detaljeret information om, hvad der sker under rotationen:

```bash
logrotate -v /etc/logrotate.conf
```

### 4. Dry run
For at se, hvad der ville ske uden at udføre ændringer:

```bash
logrotate -d /etc/logrotate.conf
```

## Tips
- Sørg for at have en korrekt konfigureret `logrotate.conf` fil for at undgå problemer med logfiler.
- Overvej at planlægge `logrotate` til at køre dagligt via cron for at holde logfilerne opdaterede.
- Tjek regelmæssigt logfilerne for at sikre, at rotationen fungerer som forventet.