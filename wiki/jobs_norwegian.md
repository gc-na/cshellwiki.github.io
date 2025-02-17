# [Linux] Bash jobs bruk: Vise bakgrunnsjobber

## Oversikt
`jobs`-kommandoen brukes i Bash for å vise statusen til bakgrunnsjobber i den nåværende terminalsesjonen. Den gir en liste over jobber som kjører i bakgrunnen, samt deres tilstand, som kan være "kjørende", "stoppet" eller "avsluttet".

## Bruk
Den grunnleggende syntaksen for `jobs`-kommandoen er:

```bash
jobs [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l`: Viser jobbenes prosess-ID (PID) sammen med jobbinformasjonen.
- `-n`: Viser bare jobber som har endret status siden forrige gang `jobs` ble kjørt.
- `-p`: Viser bare prosess-IDene til jobber.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `jobs`-kommandoen:

1. **Vise alle bakgrunnsjobber**:
   ```bash
   jobs
   ```

2. **Vise jobber med prosess-ID**:
   ```bash
   jobs -l
   ```

3. **Vise kun jobber som har endret status**:
   ```bash
   jobs -n
   ```

4. **Vise bare prosess-IDene til jobber**:
   ```bash
   jobs -p
   ```

## Tips
- Bruk `bg`-kommandoen for å fortsette en stoppet jobb i bakgrunnen etter å ha sett den med `jobs`.
- Kombiner `jobs` med `fg` for å bringe en bakgrunnsjobb tilbake til forgrunnen.
- Husk at `jobs` kun viser jobber som er startet i den nåværende terminalsesjonen. Jobber fra andre terminaler vil ikke bli vist.