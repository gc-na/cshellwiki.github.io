# [Linux] Bash htop brug: Overvåg systemressourcer

## Oversigt
htop er et interaktivt procesovervågningsværktøj, der giver brugerne mulighed for at se og administrere systemprocesser i realtid. Det er en forbedret version af den klassiske `top`-kommando og tilbyder en mere brugervenlig grænseflade med farver og mulighed for at navigere mellem processer.

## Brug
Den grundlæggende syntaks for htop-kommandoen er som følger:

```bash
htop [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h`, `--help`: Viser hjælp og oplysninger om brugen af htop.
- `-s`, `--sort`: Sorterer processerne efter den angivne kolonne (f.eks. PID, CPU, MEM).
- `-p`, `--pid`: Viser kun processer med de angivne PID'er.
- `-C`, `--no-color`: Kører htop uden farver.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge htop:

1. **Start htop**:
   ```bash
   htop
   ```

2. **Vis hjælp**:
   ```bash
   htop -h
   ```

3. **Sortér processer efter CPU-forbrug**:
   ```bash
   htop -s PERCENT_CPU
   ```

4. **Vis specifikke processer ved hjælp af PID**:
   ```bash
   htop -p 1234,5678
   ```

5. **Kør htop uden farver**:
   ```bash
   htop -C
   ```

## Tips
- Brug piletasterne til at navigere mellem processerne og tryk på `F9` for at dræbe en proces.
- Tryk på `F2` for at åbne opsætningsmenuen, hvor du kan tilpasse visningen.
- Overvåg systemets hukommelsesforbrug og CPU-belastning for at identificere flaskehalse i ydeevnen.