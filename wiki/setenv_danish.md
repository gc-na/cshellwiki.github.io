# [Linux] Bash setenv brug: Sætte miljøvariabler

## Oversigt
`setenv`-kommandoen bruges til at oprette eller ændre miljøvariabler i en shell-session. Det er en del af C-shell (csh) og kan ikke bruges direkte i Bourne-shell (sh) eller Bash. I Bash kan man bruge `export` til at opnå lignende funktionalitet.

## Brug
Den grundlæggende syntaks for `setenv`-kommandoen er:

```bash
setenv [variabelnavn] [værdi]
```

## Almindelige muligheder
`setenv` har ikke mange muligheder, da det primært bruges til at sætte variabler. Her er de mest almindelige anvendelser:

- **[variabelnavn]**: Navnet på den miljøvariabel, du vil oprette eller ændre.
- **[værdi]**: Den værdi, du vil tildele til variablen.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `setenv`:

1. Sætte en variabel for Java-hjem:
   ```bash
   setenv JAVA_HOME /usr/lib/jvm/java-11-openjdk
   ```

2. Tilføje en sti til PATH-variablen:
   ```bash
   setenv PATH $PATH:/usr/local/bin
   ```

3. Sætte en variabel for en database:
   ```bash
   setenv DB_NAME my_database
   ```

## Tips
- Husk, at `setenv` kun fungerer i C-shell og ikke i Bash. Hvis du bruger Bash, skal du bruge `export` i stedet.
- For at se alle miljøvariabler, kan du bruge `printenv`-kommandoen.
- Vær opmærksom på, at ændringer foretaget med `setenv` kun gælder for den aktuelle shell-session. For at gøre dem permanente, skal du tilføje dem til din shell-konfigurationsfil, som `.cshrc`.