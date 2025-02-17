# [Linux] Bash pwd brug: Vis den aktuelle arbejdsmappe

## Oversigt
`pwd` (print working directory) er en Bash-kommando, der viser den nuværende arbejdsmappe i terminalen. Det er en nyttig kommando, når du vil bekræfte, hvor du befinder dig i filsystemet.

## Brug
Den grundlæggende syntaks for `pwd`-kommandoen er:

```
pwd [options] [arguments]
```

## Almindelige muligheder
- `-L`: Viser den logiske sti til den aktuelle arbejdsmappe.
- `-P`: Viser den fysiske sti til den aktuelle arbejdsmappe, hvilket kan være nyttigt, hvis der er symboliske links.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `pwd`:

1. **Vis den nuværende arbejdsmappe**:
   ```bash
   pwd
   ```

2. **Vis den logiske sti**:
   ```bash
   pwd -L
   ```

3. **Vis den fysiske sti**:
   ```bash
   pwd -P
   ```

## Tips
- Brug `pwd` regelmæssigt for at holde styr på din placering i filsystemet, især når du navigerer gennem mange mapper.
- Kombiner `pwd` med andre kommandoer som `cd` for at sikre, at du altid ved, hvor du er, når du skifter mapper.
- Hvis du arbejder med scripts, kan du gemme outputtet fra `pwd` i en variabel for senere brug.