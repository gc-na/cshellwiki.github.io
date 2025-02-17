# [Linux] Bash cmp brug: Sammenlign filer byte-for-byte

## Oversigt
`cmp` er et Bash-kommando, der bruges til at sammenligne to filer byte-for-byte. Den viser, hvor de første forskelle mellem filerne findes, hvilket gør det til et nyttigt værktøj til at identificere ændringer i filer.

## Brug
Den grundlæggende syntaks for `cmp`-kommandoen er:

```bash
cmp [muligheder] [argumenter]
```

## Almindelige muligheder
- `-l`: Vis byte-positionerne og værdierne af de forskellige bytes.
- `-s`: Tjekker kun, om filerne er forskellige, uden at vise forskellene.
- `-i OFFSET`: Begynd sammenligningen fra den angivne byte-offset.
- `-n NUM`: Sammenlign kun de første NUM bytes af filerne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `cmp`:

1. **Sammenlign to filer**:
   ```bash
   cmp fil1.txt fil2.txt
   ```

2. **Sammenlign to filer og vis kun om de er forskellige**:
   ```bash
   cmp -s fil1.txt fil2.txt
   ```

3. **Vis forskelle med byte-positioner**:
   ```bash
   cmp -l fil1.txt fil2.txt
   ```

4. **Sammenlign fra en bestemt byte-offset**:
   ```bash
   cmp -i 10 fil1.txt fil2.txt
   ```

5. **Sammenlign kun de første 100 bytes**:
   ```bash
   cmp -n 100 fil1.txt fil2.txt
   ```

## Tips
- Brug `-s` flaget, hvis du kun er interesseret i at vide, om filerne er forskellige, uden at se detaljerne.
- For store filer kan `cmp` være hurtigere end andre sammenligningsværktøjer, da det stopper ved den første forskel.
- Kombiner `cmp` med andre værktøjer som `diff` for at få en mere detaljeret sammenligning, hvis det er nødvendigt.