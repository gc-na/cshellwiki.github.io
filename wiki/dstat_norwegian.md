# [Linux] Bash dstat bruk: overvåke systemytelse

## Oversikt
`dstat` er et kraftig verktøy for sanntidsovervåking av systemytelse. Det kombinerer funksjonaliteten til flere andre verktøy som `vmstat`, `iostat`, `netstat` og `ifstat`, og gir en omfattende oversikt over systemressurser som CPU-bruk, minnebruk, diskaktivitet og nettverksytelse.

## Bruk
Den grunnleggende syntaksen for `dstat` er som følger:

```bash
dstat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c` : Vis CPU-statistikk.
- `-d` : Vis diskstatistikk.
- `-n` : Vis nettverksstatistikk.
- `-m` : Vis minnebruk.
- `-t` : Vis tidsstempel for hver rad med utdata.
- `--full` : Vis alle tilgjengelige statistikker.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `dstat`:

1. **Vis CPU- og minnebruk:**

   ```bash
   dstat -c -m
   ```

2. **Vis disk- og nettverksaktivitet:**

   ```bash
   dstat -d -n
   ```

3. **Vis alle tilgjengelige statistikker med tidsstempel:**

   ```bash
   dstat --full -t
   ```

4. **Overvåk systemytelse over tid:**

   ```bash
   dstat -t --cpu --disk --net
   ```

## Tips
- Bruk `dstat` sammen med `grep` for å filtrere ut spesifikke data.
- Kjør `dstat` i bakgrunnen for å overvåke systemet mens du utfører andre oppgaver.
- Lagre utdataene til en fil for senere analyse ved å bruke omdirigering: 

   ```bash
   dstat -t > dstat_output.txt
   ```

`dstat` er et nyttig verktøy for systemadministratorer og utviklere som ønsker å få en rask oversikt over systemytelsen.