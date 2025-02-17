# [Linux] Bash passwd brug: Ændre brugerkontoadgangskode

## Oversigt
`passwd`-kommandoen bruges til at ændre adgangskoden for en bruger på et Linux-system. Det kan anvendes af både systemadministratorer og almindelige brugere til at opdatere deres egne adgangskoder.

## Brug
Den grundlæggende syntaks for `passwd`-kommandoen er som følger:

```bash
passwd [muligheder] [bruger]
```

## Almindelige muligheder
- `-d`: Slet adgangskoden for brugeren, hvilket gør kontoen uden adgangskode.
- `-e`: Tving brugeren til at ændre adgangskoden ved næste login.
- `-l`: Lås brugerkontoen ved at tilføje et "!" til adgangskoden.
- `-u`: Lås op for en låst brugerkonto.
- `-n`: Angiv det minimale antal dage mellem ændringer af adgangskoden.
- `-x`: Angiv det maksimale antal dage, før adgangskoden skal ændres.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `passwd`-kommandoen:

1. **Ændre din egen adgangskode:**
   ```bash
   passwd
   ```

2. **Ændre en anden brugers adgangskode (kræver root-rettigheder):**
   ```bash
   sudo passwd brugernavn
   ```

3. **Tving en bruger til at ændre adgangskoden ved næste login:**
   ```bash
   sudo passwd -e brugernavn
   ```

4. **Lås en brugerkonto:**
   ```bash
   sudo passwd -l brugernavn
   ```

5. **Lås op for en brugerkonto:**
   ```bash
   sudo passwd -u brugernavn
   ```

## Tips
- Sørg for at vælge en stærk adgangskode, der kombinerer bogstaver, tal og specialtegn.
- Brug `passwd -n` og `passwd -x` for at styre, hvor ofte adgangskoder skal ændres, hvilket kan forbedre sikkerheden.
- Hvis du er systemadministrator, skal du være forsigtig med at ændre andres adgangskoder og informere brugerne om ændringerne.