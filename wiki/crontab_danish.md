# [Linux] Bash crontab brug: Planlægning af opgaver

## Oversigt
`crontab`-kommandoen bruges til at planlægge og automatisere opgaver på et Unix-lignende system. Den giver brugerne mulighed for at køre scripts eller kommandoer på bestemte tidspunkter eller med faste intervaller.

## Brug
Den grundlæggende syntaks for `crontab`-kommandoen er:

```bash
crontab [muligheder] [argumenter]
```

## Almindelige muligheder
- `-e`: Rediger den aktuelle crontab-fil for den bruger, der er logget ind.
- `-l`: Vis den aktuelle crontab-fil for den bruger, der er logget ind.
- `-r`: Slet den aktuelle crontab-fil for den bruger, der er logget ind.
- `-i`: Bekræft sletning af crontab-filen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `crontab`:

1. **Rediger crontab-filen:**
   For at redigere din crontab-fil kan du bruge:
   ```bash
   crontab -e
   ```

2. **Vis din nuværende crontab:**
   For at se de opgaver, du har planlagt, kan du køre:
   ```bash
   crontab -l
   ```

3. **Slet din crontab:**
   For at slette alle planlagte opgaver, brug:
   ```bash
   crontab -r
   ```

4. **Planlæg en opgave til at køre dagligt kl. 2 om natten:**
   For at køre et script hver dag kl. 2, tilføj følgende linje i crontab:
   ```bash
   0 2 * * * /sti/til/din/script.sh
   ```

5. **Planlæg en opgave til at køre hvert 5. minut:**
   For at køre en kommando hvert 5. minut, tilføj:
   ```bash
   */5 * * * * /sti/til/kommando
   ```

## Tips
- Sørg for at angive den fulde sti til scripts eller kommandoer for at undgå problemer med miljøvariabler.
- Brug kommentarer i din crontab-fil ved at starte linjer med `#` for at gøre det lettere at forstå, hvad hver opgave gør.
- Tjek logfiler for at se output fra dine cron-job, hvis de ikke kører som forventet.