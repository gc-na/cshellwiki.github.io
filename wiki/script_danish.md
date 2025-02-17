# [Linux] Bash script brug: Optag terminal session

## Oversigt
`script` er et Bash-kommando, der bruges til at optage en terminalsession. Det gemmer alt, hvad der vises på skærmen, så du kan gennemgå det senere. Dette er nyttigt til at dokumentere processer, fejlfinde eller dele sessioner med andre.

## Brug
Den grundlæggende syntaks for `script`-kommandoen er:

```bash
script [muligheder] [filnavn]
```

## Almindelige muligheder
- `-a`: Tilføj output til en eksisterende fil i stedet for at overskrive den.
- `-q`: Kør i stille tilstand, hvilket betyder, at der ikke vises nogen besked om, at optagelsen er startet eller stoppet.
- `-t`: Gem tidsstempler for hver linje i outputfilen.

## Almindelige eksempler

1. **Optag en session til en fil:**
   ```bash
   script session.txt
   ```
   Dette starter en ny session og gemmer output i `session.txt`.

2. **Optag en session og tilføj til en eksisterende fil:**
   ```bash
   script -a session.txt
   ```
   Dette tilføjer output til `session.txt` i stedet for at overskrive den.

3. **Kør i stille tilstand:**
   ```bash
   script -q session.txt
   ```
   Dette optager sessionen uden at vise beskeder om optagelsen.

4. **Optag med tidsstempler:**
   ```bash
   script -t session.txt
   ```
   Dette gemmer tidsstempler sammen med output i `session.txt`.

## Tips
- Brug `exit`-kommandoen for at afslutte optagelsen og gemme filen.
- Gennemgå den optagede fil med `cat` eller `less` for at se indholdet.
- Overvej at bruge `script` sammen med andre kommandoer for at dokumentere komplekse processer.