# [Linux] Bash kill brug: Dræb processer ved hjælp af deres ID

## Oversigt
`kill`-kommandoen bruges til at sende signaler til processer, typisk for at afslutte dem. Det er en vigtig del af systemadministration og fejlfinding, da det giver brugeren mulighed for at styre kørende processer.

## Brug
Den grundlæggende syntaks for `kill`-kommandoen er:

```bash
kill [options] [arguments]
```

## Almindelige muligheder
- `-l`: Vis en liste over alle signaler.
- `-s SIGNAL`: Angiv det signal, der skal sendes (f.eks. `SIGKILL`).
- `-n`: Angiv signalet ved dets nummer i stedet for navnet.

## Almindelige eksempler
1. **Dræb en proces ved hjælp af dens PID:**
   For at dræbe en proces med PID 1234, kan du bruge:
   ```bash
   kill 1234
   ```

2. **Dræb en proces med et specifikt signal:**
   For at sende `SIGKILL` til en proces med PID 5678, kan du bruge:
   ```bash
   kill -s SIGKILL 5678
   ```

3. **Dræb alle processer med et bestemt navn:**
   For at dræbe alle processer kaldet `myapp`, kan du kombinere `pkill` med navnet:
   ```bash
   pkill myapp
   ```

4. **Vis alle tilgængelige signaler:**
   For at se en liste over alle signaler, kan du bruge:
   ```bash
   kill -l
   ```

## Tips
- Vær forsigtig med at bruge `SIGKILL`, da det tvinger processen til at afslutte uden at rense op.
- Brug `ps`-kommandoen til at finde PID'er på processer, før du bruger `kill`.
- Overvej at bruge `killall` til at dræbe alle forekomster af en proces ved navn, hvilket kan være lettere end at finde PID'er.