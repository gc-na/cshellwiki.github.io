# [Linux] Bash lvs bruksområde: Vise logiske volumstatus

## Oversikt
`lvs`-kommandoen brukes til å vise informasjon om logiske volum i Logical Volume Manager (LVM) på Linux-systemer. Den gir en oversikt over de logiske volumene, inkludert deres størrelse, status og tilknyttede volumgrupper.

## Bruk
Den grunnleggende syntaksen for `lvs`-kommandoen er som følger:

```bash
lvs [alternativer] [argumenter]
```

## Vanlige alternativer
- `-o` : Angi hvilke kolonner som skal vises.
- `-a` : Vis alle logiske volum, inkludert de som er skjulte.
- `-n` : Vis spesifikke logiske volum ved å angi navn.
- `--units` : Angi enheter for størrelsesvisning (f.eks. kB, MB, GB).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `lvs`-kommandoen:

1. **Vis alle logiske volum i systemet:**
   ```bash
   lvs
   ```

2. **Vis spesifikke kolonner (navn og størrelse):**
   ```bash
   lvs -o lv_name,size
   ```

3. **Vis alle logiske volum, inkludert skjulte:**
   ```bash
   lvs -a
   ```

4. **Vis logiske volum med spesifikke enheter:**
   ```bash
   lvs --units g
   ```

5. **Vis informasjon om et spesifikt logisk volum:**
   ```bash
   lvs -n mitt_logiske_volum
   ```

## Tips
- Bruk `man lvs` for å få mer detaljert informasjon om kommandoen og dens alternativer.
- Kombiner `lvs` med andre LVM-kommandoer for mer omfattende administrasjon av volumene.
- Vær oppmerksom på at du må ha nødvendige privilegier for å se informasjon om logiske volum.