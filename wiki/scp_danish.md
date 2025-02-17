# [Linux] Bash scp brug: Overførsel af filer sikkert mellem systemer

## Oversigt
`scp` (Secure Copy Protocol) er en kommandolinjeværktøj, der bruges til at overføre filer mellem lokale og fjerntliggende systemer over SSH (Secure Shell). Det sikrer, at dataene overføres sikkert ved at kryptere dem under transporten.

## Brug
Den grundlæggende syntaks for `scp`-kommandoen er:

```bash
scp [muligheder] [kilde] [destination]
```

## Almindelige muligheder
- `-r`: Kopier mapper rekursivt.
- `-P [port]`: Angiv en port, hvis SSH-serveren kører på en anden port end standardporten (22).
- `-i [fil]`: Angiv en specifik identitetsfil (privat nøgle) til autentificering.
- `-v`: Aktiver detaljeret output for fejlfinding.

## Almindelige eksempler
1. **Kopier en fil fra lokal til fjernserver:**
   ```bash
   scp /sti/til/lokal/fil.txt bruger@fjernserver:/sti/til/destination/
   ```

2. **Kopier en fil fra fjernserver til lokal maskine:**
   ```bash
   scp bruger@fjernserver:/sti/til/fjern/fil.txt /sti/til/lokal/destination/
   ```

3. **Kopier en hel mappe fra lokal til fjernserver:**
   ```bash
   scp -r /sti/til/lokal/mappe bruger@fjernserver:/sti/til/destination/
   ```

4. **Kopier en fil til en specifik port:**
   ```bash
   scp -P 2222 /sti/til/lokal/fil.txt bruger@fjernserver:/sti/til/destination/
   ```

5. **Brug en specifik identitetsfil:**
   ```bash
   scp -i /sti/til/nøgle.pem /sti/til/lokal/fil.txt bruger@fjernserver:/sti/til/destination/
   ```

## Tips
- Sørg for, at SSH-serveren er korrekt konfigureret på fjernsystemet for at undgå forbindelsesproblemer.
- Brug `-v`-muligheden, hvis du oplever problemer, da det giver nyttige fejlinformationer.
- Overvej at bruge `rsync` til store filoverførsler, da det kan være mere effektivt ved at kun overføre ændrede data.