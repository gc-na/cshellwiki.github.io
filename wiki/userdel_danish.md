# [Linux] Bash userdel brug: Slet brugerkonti

## Oversigt
`userdel`-kommandoen bruges til at slette en brugerkonto fra systemet. Det fjerner brugerens oplysninger fra systemets brugerdatabase og kan også fjerne brugerens hjemmemappe, afhængigt af de valgte indstillinger.

## Brug
Den grundlæggende syntaks for `userdel`-kommandoen er som følger:

```bash
userdel [muligheder] [brugernavn]
```

## Almindelige muligheder
- `-r`: Sletter brugerens hjemmemappe og mail-spool.
- `-f`: Tvinger sletning af brugeren, selvom brugeren er logget ind.
- `-Z`: Angiver SELinux sikkerhedskonteksten for brugeren.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `userdel`:

1. Slet en bruger uden at fjerne hjemmemappen:
   ```bash
   userdel brugernavn
   ```

2. Slet en bruger og fjern samtidig hjemmemappen:
   ```bash
   userdel -r brugernavn
   ```

3. Tving sletning af en bruger, der er logget ind:
   ```bash
   userdel -f brugernavn
   ```

4. Slet en bruger og angiv en SELinux sikkerhedskontekst:
   ```bash
   userdel -Z sikkerhedskontekst brugernavn
   ```

## Tips
- Sørg for at tage backup af vigtige data, før du sletter en bruger.
- Tjek, at brugeren ikke er logget ind, hvis du ikke bruger `-f`-muligheden.
- Overvej at bruge `userdel -r` for at rydde op i systemet og fjerne alle relaterede filer.