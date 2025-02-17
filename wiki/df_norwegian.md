# [Linux] Bash df Bruk: Vise diskplassbruk

## Oversikt
`df`-kommandoen brukes til å vise informasjon om diskplassbruk på filsystemene i Linux. Den gir en oversikt over hvor mye plass som er brukt og hvor mye som er tilgjengelig på hver montert enhet.

## Bruk
Grunnleggende syntaks for `df`-kommandoen er som følger:
```
df [alternativer] [argumenter]
```

## Vanlige Alternativer
- `-h`: Viser diskplass i "menneskelig lesbar" format (f.eks. MB, GB).
- `-T`: Viser filsystemtype sammen med diskplassinformasjonen.
- `-a`: Viser informasjon om alle filsystemer, inkludert de som har 0 brukt plass.
- `-i`: Viser informasjon om inode-bruk i stedet for diskplass.

## Vanlige Eksempler
- Vise diskplassbruk for alle monterte filsystemer:
  ```bash
  df
  ```

- Vise diskplass i menneskelig lesbar format:
  ```bash
  df -h
  ```

- Vise diskplass med filsystemtype:
  ```bash
  df -T
  ```

- Vise informasjon om alle filsystemer, inkludert de som ikke er i bruk:
  ```bash
  df -a
  ```

- Vise inode-bruk:
  ```bash
  df -i
  ```

## Tips
- Bruk `df -h` for å få en rask oversikt over diskplass som er lett å forstå.
- Kombiner `df` med `grep` for å filtrere spesifikke filsystemer, for eksempel:
  ```bash
  df -h | grep /dev/sda1
  ```
- Sjekk diskplass regelmessig for å unngå at systemet går tom for plass, noe som kan føre til ytelsesproblemer.