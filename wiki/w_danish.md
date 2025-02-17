# [Linux] Bash w brug: Vis brugerinformasjon

## Oversigt
`w`-kommandoen bruges til at vise, hvilke brugere der er logget ind på systemet, samt deres aktive sessioner. Den giver også information om, hvor længe de har været aktive, og hvad de laver i øjeblikket.

## Brug
Den grundlæggende syntaks for `w`-kommandoen er:

```bash
w [options] [arguments]
```

## Almindelige muligheder
- `-h`: Udelader overskriften fra output.
- `-s`: Viser en kortere version af output.
- `-f`: Viser fulde navne på terminaler.
- `-u`: Viser brugeren, der ejer terminalen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `w`-kommandoen kan bruges:

1. **Vis alle loggede brugere:**
   ```bash
   w
   ```

2. **Vis brugere uden overskrift:**
   ```bash
   w -h
   ```

3. **Vis en kort version af brugerinformation:**
   ```bash
   w -s
   ```

4. **Vis brugere med fulde terminalnavne:**
   ```bash
   w -f
   ```

5. **Vis brugere med ejerinformation:**
   ```bash
   w -u
   ```

## Tips
- Brug `w` regelmæssigt for at overvåge systemaktivitet og se, hvilke brugere der er aktive.
- Kombiner `w` med andre kommandolinjeværktøjer som `grep` for at filtrere specifikke brugere.
- Overvej at bruge `w` i scripts for at logge brugeraktivitet på systemet.