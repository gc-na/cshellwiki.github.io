# [Linux] Bash bg Bruk: Fortsetter bakgrunnsprosesser

## Oversikt
`bg`-kommandoen brukes i Bash for å fortsette en stoppet prosess i bakgrunnen. Dette er nyttig når du har startet en prosess i forgrunnen og ønsker å la den kjøre mens du fortsetter å bruke terminalen til andre oppgaver.

## Bruk
Den grunnleggende syntaksen for `bg`-kommandoen er som følger:

```bash
bg [job_id]
```

## Vanlige alternativer
- `job_id`: Identifikatoren for jobben du ønsker å fortsette i bakgrunnen. Hvis du ikke spesifiserer en job_id, vil `bg` fortsette den sist stoppede jobben.

## Vanlige eksempler

### Fortsett den sist stoppede jobben
For å fortsette den sist stoppede jobben i bakgrunnen, kan du bruke:

```bash
bg
```

### Fortsett en spesifikk jobb
Hvis du har flere stoppede jobber og ønsker å fortsette en spesifikk, kan du bruke job_id. For eksempel, hvis job_id er 1:

```bash
bg %1
```

### Se jobber
Før du bruker `bg`, kan det være nyttig å se hvilke jobber som er stoppet. Du kan bruke `jobs`-kommandoen:

```bash
jobs
```

### Kombinere med andre kommandoer
Du kan også kombinere `bg` med `ctrl+z` for å stoppe en prosess og deretter fortsette den i bakgrunnen:

```bash
# Start en prosess
sleep 100

# Stopp prosessen med Ctrl+Z
# Fortsett prosessen i bakgrunnen
bg
```

## Tips
- Husk at du kan bruke `jobs` for å se status på jobber før du bruker `bg`.
- Vær oppmerksom på at prosesser som kjører i bakgrunnen kan skrive ut til terminalen. Bruk `nohup` hvis du vil unngå dette.
- Du kan bruke `fg`-kommandoen for å bringe en bakgrunnsprosess tilbake til forgrunnen hvis du trenger å interagere med den.