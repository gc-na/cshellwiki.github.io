# [Linux] Bash tty brug: viser terminalens navn

## Oversigt
`tty` er en Bash-kommando, der bruges til at vise navnet på den terminal, som brugeren er tilsluttet. Dette kan være nyttigt til fejlfinding eller når man arbejder med flere terminalvinduer.

## Brug
Den grundlæggende syntaks for `tty`-kommandoen er:

```bash
tty [options] [arguments]
```

## Almindelige muligheder
- `-s`: Kør i stille tilstand, hvilket betyder, at der ikke vises nogen output.
- `--help`: Vis hjælp og information om brugen af kommandoen.
- `--version`: Vis versionen af `tty`.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `tty`:

1. **Vis terminalnavn**:
   For at se navnet på den nuværende terminal kan du blot køre:
   ```bash
   tty
   ```

2. **Brug i scripts**:
   Du kan bruge `tty` i et script for at gemme terminalnavnet i en variabel:
   ```bash
   terminal_name=$(tty)
   echo "Du arbejder på terminal: $terminal_name"
   ```

3. **Stille tilstand**:
   Hvis du kun ønsker at kontrollere, om du er i en terminal uden output, kan du bruge:
   ```bash
   tty -s && echo "Du er i en terminal"
   ```

## Tips
- Brug `tty` til at bekræfte, at du arbejder i den rigtige terminal, især når du kører scripts, der kan påvirke systemet.
- Kombiner `tty` med andre kommandoer i scripts for at gøre dem mere dynamiske og interaktive.
- Husk at `tty` kun viser terminalnavnet og ikke yderligere oplysninger om terminalens tilstand.