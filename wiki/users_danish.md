# [Linux] Bash-brugere kommando: Vis brugere på systemet

## Oversigt
Kommandoen `users` viser en liste over brugernavne, der i øjeblikket er logget ind på systemet. Det er en nyttig kommando til hurtigt at få indsigt i, hvilke brugere der er aktive på en Linux-maskine.

## Brug
Den grundlæggende syntaks for kommandoen er:

```bash
users [options] [arguments]
```

## Almindelige muligheder
- `-a`: Vis alle brugernavne, inklusive dem, der er logget ind via en terminal.
- `-r`: Vis kun brugere, der har en aktiv session.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `users`-kommandoen:

1. **Vis aktive brugere**:
   ```bash
   users
   ```

2. **Vis alle brugere, inklusive dem med terminalsessioner**:
   ```bash
   users -a
   ```

3. **Vis kun brugere med aktive sessioner**:
   ```bash
   users -r
   ```

## Tips
- Brug `who`-kommandoen sammen med `users` for at få flere oplysninger om de aktive brugere, såsom deres login-tid og terminal.
- Hvis du vil se en liste over alle brugere på systemet, kan du se i `/etc/passwd`-filen i stedet for at bruge `users`.