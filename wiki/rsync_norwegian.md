# [Linux] Bash rsync Bruk: Synkronisering av filer og kataloger

## Oversikt
Rsync er et kraftig verktøy for å synkronisere filer og kataloger mellom to steder, enten lokalt eller over et nettverk. Det er kjent for sin effektivitet, da det bare overfører endrede deler av filer, noe som sparer tid og båndbredde.

## Bruk
Den grunnleggende syntaksen for rsync-kommandoen er som følger:

```bash
rsync [alternativer] [kilde] [mål]
```

## Vanlige alternativer
- `-a`: Arkivmodus; kopierer filer og kataloger rekursivt og bevarer metadata.
- `-v`: Vis detaljert utdata under overføring.
- `-z`: Komprimerer data under overføring for å spare båndbredde.
- `-r`: Rekursiv kopiering av kataloger.
- `--delete`: Sletter filer i målplasseringen som ikke finnes i kildeplasseringen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke rsync:

1. **Kopiere en fil fra lokal til lokal katalog:**
   ```bash
   rsync -av /sti/til/kildefil.txt /sti/til/målmappe/
   ```

2. **Synkronisere en lokal katalog med en ekstern server:**
   ```bash
   rsync -avz /sti/til/lokalmappe/ bruker@server:/sti/til/målmappe/
   ```

3. **Kopiere filer fra en ekstern server til lokal maskin:**
   ```bash
   rsync -avz bruker@server:/sti/til/kildefil.txt /sti/til/målmappe/
   ```

4. **Synkronisere to kataloger og slette filer i mål som ikke finnes i kilde:**
   ```bash
   rsync -av --delete /sti/til/kilde/ /sti/til/mål/
   ```

## Tips
- Bruk `-n` (eller `--dry-run`) for å se hva som vil bli gjort uten å utføre handlingene. Dette er nyttig for å unngå uventede endringer.
- Sørg for å bruke en avsluttende skråstrek (`/`) på kildebanen hvis du ønsker å synkronisere innholdet i katalogen, ikke selve katalogen.
- Vurder å bruke SSH for sikker overføring ved å spesifisere `-e ssh` når du synkroniserer over nettverket.