# [Linux] Bash unalias brug: Fjerner aliaser

## Oversigt
`unalias` kommandoen bruges til at fjerne aliaser, der er blevet oprettet i den nuværende shell-session. Aliaser er genveje til kommandoer, som kan gøre det lettere at udføre ofte brugte kommandoer med kortere syntaks.

## Brug
Den grundlæggende syntaks for `unalias` kommandoen er:

```bash
unalias [options] [arguments]
```

## Almindelige muligheder
- `-a`: Fjerner alle aliaser i den nuværende session.
- `-m`: Fjerner aliaser, der matcher et givet mønster.

## Almindelige eksempler

1. **Fjerne et specifikt alias:**
   Hvis du har et alias kaldet `ls` til `ls -la`, kan du fjerne det med følgende kommando:
   ```bash
   unalias ls
   ```

2. **Fjerne alle aliaser:**
   For at fjerne alle aliaser, kan du bruge:
   ```bash
   unalias -a
   ```

3. **Fjerne aliaser, der matcher et mønster:**
   Hvis du vil fjerne aliaser, der starter med `g`, kan du gøre det med:
   ```bash
   unalias g*
   ```

## Tips
- Brug `alias` kommandoen først for at se, hvilke aliaser der er aktive, før du fjerner dem.
- Vær opmærksom på, at når du fjerner et alias, vil den oprindelige kommando blive genoprettet, så sørg for at du ikke fjerner noget, du stadig har brug for.
- Overvej at tilføje aliaser til din `.bashrc` fil, hvis du ofte bruger dem, så de automatisk bliver tilgængelige i fremtidige sessioner.