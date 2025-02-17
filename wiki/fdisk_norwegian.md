# [Linux] Bash fdisk Bruk: Verktøy for partisjonering av disk

## Oversikt
`fdisk` er et kommandolinjeverktøy som brukes til å opprette, slette og endre partisjoner på harddisker. Det gir brukeren mulighet til å administrere partisjoner på en enkel og effektiv måte.

## Bruk
Den grunnleggende syntaksen for `fdisk` er som følger:

```bash
fdisk [alternativer] [enhet]
```

Her refererer `[enhet]` til den spesifikke disken du ønsker å administrere, for eksempel `/dev/sda`.

## Vanlige alternativer
- `-l`: Viser en liste over alle partisjoner på systemet.
- `-u`: Bruker sektorer i stedet for kilobyte for å vise partisjonsstørrelser.
- `-n`: Oppretter en ny partisjon.
- `-d`: Sletter en eksisterende partisjon.
- `-t`: Endrer partisjonstype.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `fdisk` kan brukes:

1. **Liste alle partisjoner på en disk:**
   ```bash
   fdisk -l /dev/sda
   ```

2. **Opprette en ny partisjon:**
   ```bash
   fdisk /dev/sda
   # Deretter følg instruksjonene i interaktiv modus for å opprette en ny partisjon.
   ```

3. **Slette en eksisterende partisjon:**
   ```bash
   fdisk /dev/sda
   # Velg 'd' for å slette partisjonen og følg instruksjonene.
   ```

4. **Endre partisjonstype:**
   ```bash
   fdisk /dev/sda
   # Velg 't' for å endre partisjonstype og angi partisjonsnummeret.
   ```

## Tips
- **Sikkerhetskopier data:** Før du gjør endringer med `fdisk`, sørg for å sikkerhetskopiere viktige data for å unngå tap.
- **Bruk med forsiktighet:** `fdisk` kan endre diskens struktur, så vær sikker på hva du gjør før du utfører kommandoene.
- **Les dokumentasjonen:** Bruk `man fdisk` for å få mer informasjon om tilgjengelige alternativer og bruksområder.