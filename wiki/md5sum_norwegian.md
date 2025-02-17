# [Linux] Bash md5sum bruk: Generere MD5-hash for filer

## Oversikt
`md5sum` er et Bash-kommandoverktøy som brukes til å generere MD5-hashverdier for filer. MD5-hash er en 128-biters hashverdi som ofte brukes for å verifisere integriteten til data og filer.

## Bruk
Grunnleggende syntaks for `md5sum`-kommandoen er som følger:
```
md5sum [alternativer] [argumenter]
```

## Vanlige alternativer
- `-b`: Behandle filene som binære.
- `-c`: Kontroller MD5-hashverdier fra en fil.
- `-t`: Behandle filene som tekstfiler.
- `--help`: Vis hjelp og tilgjengelige alternativer.
- `--version`: Vis versjonsinformasjon om md5sum.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `md5sum`:

1. Generere MD5-hash for en enkelt fil:
   ```bash
   md5sum fil.txt
   ```

2. Generere MD5-hash for flere filer:
   ```bash
   md5sum fil1.txt fil2.txt fil3.txt
   ```

3. Lagre MD5-hashverdier til en fil:
   ```bash
   md5sum fil.txt > hash.txt
   ```

4. Kontrollere MD5-hashverdier fra en fil:
   ```bash
   md5sum -c hash.txt
   ```

5. Generere MD5-hash for en binærfil:
   ```bash
   md5sum -b binarfil.bin
   ```

## Tips
- Sørg for å bruke `-c` alternativet med en hashfil for å verifisere filintegritet.
- Bruk `--help` for å få en oversikt over tilgjengelige alternativer og bruksområder.
- Vær oppmerksom på at MD5 ikke er kryptografisk sikkert for sensitive data; vurder å bruke sterkere algoritmer som SHA-256 for sikkerhetsformål.