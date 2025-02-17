# [Linux] Bash screen brug: Administrer terminal sessioner

## Oversigt
`screen` er et terminal multiplexer værktøj, der giver brugerne mulighed for at oprette, administrere og navigere mellem flere terminal sessioner fra en enkelt terminal. Det er særligt nyttigt, når man arbejder på fjernservere, da det tillader sessioner at fortsætte, selv når forbindelsen til serveren afbrydes.

## Brug
Den grundlæggende syntaks for `screen` kommandoen er som følger:

```bash
screen [options] [arguments]
```

## Almindelige muligheder
- `-S <session_name>`: Opretter en ny session med det angivne navn.
- `-d -r <session_name>`: Frakobler og genopretter en eksisterende session.
- `-list`: Viser en liste over aktive sessioner.
- `-X <command>`: Sender en kommando til en kørende session.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `screen`:

1. Opret en ny session:
   ```bash
   screen -S min_session
   ```

2. Liste aktive sessioner:
   ```bash
   screen -list
   ```

3. Genopret en frakoblet session:
   ```bash
   screen -d -r min_session
   ```

4. Udfør en kommando i en eksisterende session:
   ```bash
   screen -S min_session -X stuff "echo Hello World\n"
   ```

## Tips
- Brug `Ctrl-a` efterfulgt af `d` for at frakoble en session, så du kan vende tilbage til din terminal.
- For at afslutte en session, kan du skrive `exit` i den screen session, du ønsker at lukke.
- Overvej at navngive dine sessioner, så de er lettere at identificere, især når du arbejder med flere sessioner.