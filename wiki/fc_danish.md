# [Linux] Bash fc brug: Gendan og rediger tidligere kommandoer

## Oversigt
`fc`-kommandoen i Bash bruges til at vise, redigere og genkøre tidligere kommandoer fra kommandolinjen. Det er en nyttig funktion, når du ønsker at rette fejl eller gentage tidligere udførte kommandoer.

## Brug
Den grundlæggende syntaks for `fc`-kommandoen er:

```bash
fc [options] [arguments]
```

## Almindelige muligheder
- `-l`: List tidligere kommandoer.
- `-s`: Kør en kommando uden at vise den først.
- `-n`: Vis ikke linjenumre, når du lister kommandoer.
- `-r`: Vis kommandoer i omvendt rækkefølge.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `fc`:

1. **Liste de seneste kommandoer:**

   ```bash
   fc -l
   ```

2. **Redigere den seneste kommando i din standard teksteditor:**

   ```bash
   fc
   ```

3. **Kør den seneste kommando uden at vise den:**

   ```bash
   fc -s
   ```

4. **Liste de seneste 5 kommandoer:**

   ```bash
   fc -l -n -5
   ```

5. **Redigere den næstsidste kommando:**

   ```bash
   fc -s -2
   ```

## Tips
- Brug `fc` til hurtigt at rette tastefejl i tidligere kommandoer, hvilket kan spare tid.
- Du kan ændre din standard teksteditor ved at sætte miljøvariablen `EDITOR`, så `fc` åbner i din foretrukne editor.
- Husk at `fc` kun arbejder med kommandoer fra den nuværende session; tidligere sessioner vil ikke være tilgængelige.