# [Linux] Bash lvextend brug: Udvid logiske volumener

## Oversigt
`lvextend` er et Bash-kommando, der bruges til at udvide størrelsen på et logisk volumen i Logical Volume Manager (LVM). Dette er nyttigt, når du har brug for mere plads til dine data uden at skulle oprette et nyt volumen.

## Brug
Den grundlæggende syntaks for `lvextend`-kommandoen er:

```bash
lvextend [muligheder] [argumenter]
```

## Almindelige muligheder
- `-L +[størrelse]`: Angiver, hvor meget du vil udvide volumenet.
- `-l +[antal]`: Angiver, hvor mange logiske enheder du vil tilføje.
- `-r`: Udfør automatisk en filsystemudvidelse efter udvidelsen af volumenet.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `lvextend`:

1. **Udvid et volumen med 10 GB**:
   ```bash
   lvextend -L +10G /dev/vg_name/lv_name
   ```

2. **Udvid et volumen til en specifik størrelse**:
   ```bash
   lvextend -L 50G /dev/vg_name/lv_name
   ```

3. **Udvid et volumen med 5 logiske enheder**:
   ```bash
   lvextend -l +5 /dev/vg_name/lv_name
   ```

4. **Udvid et volumen og automatisk udvid filsystemet**:
   ```bash
   lvextend -r -L +10G /dev/vg_name/lv_name
   ```

## Tips
- Sørg for at tjekke, at der er tilstrækkelig plads i den fysiske volumengruppe, før du udvider et logisk volumen.
- Brug `lvdisplay`-kommandoen for at få oplysninger om eksisterende logiske volumener og deres størrelser.
- Overvej at tage backup af vigtige data, før du foretager ændringer i volumenstørrelser.