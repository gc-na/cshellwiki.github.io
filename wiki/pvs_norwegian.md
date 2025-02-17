# [Linux] Bash pvs bruk: Vise volumgrupper

## Oversikt
`pvs`-kommandoen brukes til å vise informasjon om fysiske volum i LVM (Logical Volume Manager). Den gir en oversikt over hvilke fysiske enheter som er tilknyttet volumgrupper og viser relevant informasjon som størrelse og status.

## Bruk
Den grunnleggende syntaksen for `pvs`-kommandoen er:

```bash
pvs [alternativer] [argumenter]
```

## Vanlige alternativer
- `-o, --options`: Angi hvilke kolonner som skal vises.
- `-h, --human-readable`: Vis størrelser i et mer lesbart format (f.eks. MB, GB).
- `-v, --verbose`: Vis mer detaljert informasjon.
- `--noheadings`: Skjul overskriftene i utdataene.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `pvs`:

1. **Vis alle fysiske volum**:
   ```bash
   pvs
   ```

2. **Vis fysiske volum med menneskelig lesbare størrelser**:
   ```bash
   pvs -h
   ```

3. **Vis spesifikke kolonner (f.eks. navn, størrelse, status)**:
   ```bash
   pvs -o pv_name,pv_size,pv_attr
   ```

4. **Vis detaljert informasjon om fysiske volum**:
   ```bash
   pvs -v
   ```

5. **Skjul overskrifter i utdataene**:
   ```bash
   pvs --noheadings
   ```

## Tips
- Bruk `-h`-alternativet for å gjøre utdataene lettere å lese, spesielt når du arbeider med store volum.
- Kombiner `pvs` med andre LVM-kommandoer for å få en mer omfattende oversikt over lagringssystemet ditt.
- Husk at `pvs` krever at LVM er installert og konfigurert på systemet ditt for å fungere korrekt.