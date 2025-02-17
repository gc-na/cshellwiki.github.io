# [Linux] Bash lsof Brug: Vise åbne filer og netværksforbindelser

## Oversigt
`lsof` (List Open Files) er et kommandolinjeværktøj, der viser en liste over alle åbne filer og de processer, der har dem åbne. Det er nyttigt til fejlfinding og overvågning af systemressourcer.

## Brug
Den grundlæggende syntaks for `lsof` er som følger:

```bash
lsof [options] [arguments]
```

## Almindelige muligheder
- `-a`: Kombinerer flere betingelser (AND).
- `-c <kommando>`: Filtrerer resultaterne til kun at vise filer åbnet af en bestemt kommando.
- `-u <bruger>`: Viser filer åbnet af en bestemt bruger.
- `-p <PID>`: Viser filer åbnet af en specifik proces ID.
- `-i`: Viser netværksforbindelser.

## Almindelige eksempler
- For at vise alle åbne filer på systemet:
  ```bash
  lsof
  ```

- For at vise filer åbnet af en bestemt bruger:
  ```bash
  lsof -u brugernavn
  ```

- For at finde ud af, hvilke filer en bestemt proces (f.eks. med PID 1234) har åbnet:
  ```bash
  lsof -p 1234
  ```

- For at vise alle netværksforbindelser:
  ```bash
  lsof -i
  ```

- For at finde ud af, hvilke processer der bruger en bestemt port (f.eks. port 80):
  ```bash
  lsof -i :80
  ```

## Tips
- Brug `lsof` med `grep` for at filtrere resultaterne yderligere. For eksempel:
  ```bash
  lsof | grep søgeord
  ```
- Vær opmærksom på, at du muligvis skal køre `lsof` med root-rettigheder for at se alle åbne filer.
- Tjek regelmæssigt åbne filer for at overvåge systemets sundhed og identificere eventuelle problemer.