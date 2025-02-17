# [Linux] Bash killall brug: Dræb processer ved navn

## Oversigt
`killall`-kommandoen bruges til at dræbe alle processer, der kører med et bestemt navn. Dette er nyttigt, når du ønsker at stoppe alle instanser af et program uden at skulle finde og dræbe dem én ad gangen.

## Brug
Den grundlæggende syntaks for `killall`-kommandoen er:

```bash
killall [muligheder] [argumenter]
```

## Almindelige muligheder
- `-u, --user <bruger>`: Dræb kun processer, der tilhører den angivne bruger.
- `-s, --signal <signal>`: Angiv det signal, der skal sendes til processerne (standard er SIGTERM).
- `-q, --quiet`: Undertrykker fejlmeddelelser, hvis ingen processer blev dræbt.
- `-I, --ignore-case`: Ignorerer store og små bogstaver i procesnavnet.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `killall` kan bruges:

1. Dræb alle instanser af Firefox:
   ```bash
   killall firefox
   ```

2. Dræb alle processer, der tilhører en bestemt bruger:
   ```bash
   killall -u brugernavn
   ```

3. Send et specifikt signal til alle instanser af et program (f.eks. SIGKILL):
   ```bash
   killall -s SIGKILL programnavn
   ```

4. Dræb alle processer med et navn, der ignorerer store og små bogstaver:
   ```bash
   killall -I programnavn
   ```

## Tips
- Vær forsigtig med at bruge `killall`, da det vil dræbe alle processer med det angivne navn, hvilket kan føre til tab af data, hvis der er gemte ændringer i et program.
- Brug `killall -q` for at undgå unødvendige fejlmeddelelser, hvis der ikke er nogen processer at dræbe.
- Overvej at bruge `pgrep`-kommandoen først for at se, hvilke processer der kører, før du dræber dem.