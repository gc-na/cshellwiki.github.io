# [Linux] Bash ulimit brug: Begræns ressourcer for processer

## Oversigt
`ulimit`-kommandoen bruges til at indstille eller vise grænser for systemressourcer, som en bruger kan anvende. Dette er nyttigt for at forhindre, at en enkelt proces bruger for mange ressourcer og dermed påvirker systemets stabilitet.

## Brug
Den grundlæggende syntaks for `ulimit`-kommandoen er som følger:

```bash
ulimit [options] [arguments]
```

## Almindelige muligheder
- `-a`: Viser alle nuværende grænser.
- `-c`: Sætter grænsen for størrelsen af core-dumps.
- `-d`: Sætter grænsen for størrelsen af det dataområde, som en proces kan bruge.
- `-f`: Sætter grænsen for størrelsen af filer, der kan oprettes.
- `-l`: Sætter grænsen for størrelsen af låste sider i hukommelsen.
- `-m`: Sætter grænsen for størrelsen af det fysiske hukommelsesområde.
- `-n`: Sætter grænsen for antallet af åbne filer.
- `-s`: Sætter stakstørrelsen for en proces.
- `-t`: Sætter grænsen for CPU-tid i sekunder.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `ulimit` kan anvendes:

1. **Vis alle nuværende grænser:**
   ```bash
   ulimit -a
   ```

2. **Sæt grænsen for åbne filer til 1024:**
   ```bash
   ulimit -n 1024
   ```

3. **Sæt grænsen for core-dumps til 0 (deaktiver):**
   ```bash
   ulimit -c 0
   ```

4. **Sæt stakstørrelsen til 8 MB:**
   ```bash
   ulimit -s 8192
   ```

5. **Vis grænsen for CPU-tid:**
   ```bash
   ulimit -t
   ```

## Tips
- Overvej at bruge `ulimit -a` for at få et overblik over alle grænser, før du foretager ændringer.
- Vær forsigtig med at sætte grænser for lavt, da det kan forhindre programmer i at fungere korrekt.
- Ændringer foretaget med `ulimit` gælder kun for den aktuelle shell-session og dens underordnede processer. For at gøre ændringerne permanente, skal du tilføje dem til din shell's konfigurationsfil (f.eks. `.bashrc` eller `.bash_profile`).