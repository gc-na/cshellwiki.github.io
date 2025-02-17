# [Linux] Bash bindkey brug: Tildel tastaturgenveje

## Oversigt
`bindkey` er en kommando, der bruges i Zsh (Z Shell) til at tildele tastaturgenveje og ændre tastaturbindings. Det giver brugerne mulighed for at tilpasse deres kommandolinjeoplevelse ved at knytte specifikke handlinger til bestemte taster.

## Brug
Den grundlæggende syntaks for `bindkey` er som følger:

```bash
bindkey [options] [arguments]
```

## Almindelige muligheder
- `-e`: Skift til emacs-tilstand for tastaturbindinger.
- `-v`: Skift til vi-tilstand for tastaturbindinger.
- `-L`: Vis alle nuværende tastaturbindinger.
- `-s`: Tildel en sekvens af taster til en handling.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `bindkey`:

1. **Vis alle nuværende tastaturbindinger:**
   ```bash
   bindkey -L
   ```

2. **Skift til emacs-tilstand:**
   ```bash
   bindkey -e
   ```

3. **Tildel en tastekombination til en kommando:**
   ```bash
   bindkey '^X^C' 'clear-screen'
   ```

4. **Tildel en sekvens af taster til en handling:**
   ```bash
   bindkey -s 'jj' 'exit\n'
   ```

## Tips
- Overvej at oprette en backup af dine nuværende tastaturbindinger, før du foretager ændringer.
- Brug `bindkey -L` ofte for at holde styr på dine bindinger og undgå konflikter.
- Eksperimenter med forskellige taster og sekvenser for at finde de mest effektive genveje til din arbejdsgang.