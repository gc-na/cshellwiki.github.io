# [Linux] Bash lvextend Bruk: Utvide logiske volum

## Oversikt
`lvextend` er en Bash-kommando som brukes til å utvide størrelsen på et logisk volum i Logical Volume Manager (LVM). Dette er nyttig når du trenger mer plass på et eksisterende volum uten å måtte opprette et nytt.

## Bruk
Den grunnleggende syntaksen for `lvextend` er som følger:

```bash
lvextend [alternativer] [argumenter]
```

## Vanlige alternativer
- `-L, --size`: Angi den nye størrelsen på volumet.
- `-l, --extents`: Angi antall extents som volumet skal utvides med.
- `-r, --resizefs`: Utvid filsystemet automatisk etter at volumet er utvidet.
- `-n, --name`: Angi navnet på det logiske volumet som skal utvides.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `lvextend`:

1. **Utvid et logisk volum til en spesifikk størrelse:**
   ```bash
   lvextend -L +10G /dev/vg01/lv_data
   ```

2. **Utvid et logisk volum med et bestemt antall extents:**
   ```bash
   lvextend -l +100 /dev/vg01/lv_data
   ```

3. **Utvid et logisk volum og samtidig utvid filsystemet:**
   ```bash
   lvextend -r -L +5G /dev/vg01/lv_data
   ```

4. **Utvid et logisk volum til maksimal tilgjengelig plass:**
   ```bash
   lvextend -l +100%FREE /dev/vg01/lv_data
   ```

## Tips
- Før du utvider et logisk volum, sørg for å ta sikkerhetskopi av viktige data.
- Bruk `lvdisplay` for å sjekke nåværende størrelse og tilgjengelig plass før du utfører endringer.
- Vær oppmerksom på at utvidelse av filsystemet kan kreve at volumet er unmounted, avhengig av filsystemtype.