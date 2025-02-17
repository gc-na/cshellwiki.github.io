# [Linux] Bash hwclock bruk: Håndter systemklokken

## Oversikt
`hwclock`-kommandoen brukes til å lese og sette systemets hardwareklokke, også kjent som RTC (Real-Time Clock). Denne klokken er uavhengig av operativsystemet og fortsetter å holde tid selv når datamaskinen er slått av.

## Bruk
Den grunnleggende syntaksen for `hwclock`-kommandoen er som følger:

```bash
hwclock [alternativer] [argumenter]
```

## Vanlige alternativer
- `--show`: Viser den nåværende tiden fra hardwareklokken.
- `--set`: Setter hardwareklokken til en spesifisert tid.
- `--hctosys`: Setter systemklokken til verdien fra hardwareklokken.
- `--systohc`: Setter hardwareklokken til verdien fra systemklokken.
- `--utc`: Angir at tiden er i UTC (Coordinated Universal Time).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `hwclock` kan brukes:

1. **Vise den nåværende tiden fra hardwareklokken:**
   ```bash
   hwclock --show
   ```

2. **Sette hardwareklokken til en spesifikk tid:**
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

3. **Sette systemklokken til verdien fra hardwareklokken:**
   ```bash
   hwclock --hctosys
   ```

4. **Sette hardwareklokken til verdien fra systemklokken:**
   ```bash
   hwclock --systohc
   ```

5. **Vise tiden i UTC-format:**
   ```bash
   hwclock --show --utc
   ```

## Tips
- Sørg for at du har administrative rettigheter når du setter eller endrer hardwareklokken.
- Det kan være lurt å synkronisere systemklokken med hardwareklokken regelmessig for å unngå tidssynkroniseringsproblemer.
- Bruk `--utc` alternativet hvis du arbeider med servere som krever UTC-tid for å unngå forvirring med tidssoner.