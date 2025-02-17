# [Linux] Bash dirname brug: Hent stien til en fil

## Oversigt
`dirname` er en Bash-kommando, der bruges til at udtrække stien til en fil eller en mappe fra en given sti. Den returnerer den del af stien, der fører til filen, hvilket kan være nyttigt i scripts og ved håndtering af filsystemer.

## Brug
Den grundlæggende syntaks for `dirname` er som følger:
```
dirname [options] [arguments]
```

## Almindelige muligheder
- `-z`, `--zero`: Angiver, at inputfilnavnene er adskilt af nul-tegn i stedet for nye linjer.
- `--help`: Viser en hjælpemeddelelse med information om brugen af kommandoen.
- `--version`: Viser versionsoplysninger om `dirname`.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `dirname`:

1. **Hente stien til en fil:**
   ```bash
   dirname /home/user/documents/file.txt
   ```
   Outputtet vil være:
   ```
   /home/user/documents
   ```

2. **Hente stien til en mappe:**
   ```bash
   dirname /var/log/syslog
   ```
   Outputtet vil være:
   ```
   /var/log
   ```

3. **Brug af dirname i et script:**
   ```bash
   FILE="/home/user/documents/file.txt"
   DIR=$(dirname "$FILE")
   echo "Stien til filen er: $DIR"
   ```
   Outputtet vil være:
   ```
   Stien til filen er: /home/user/documents
   ```

## Tips
- Brug altid anførselstegn omkring stinavne, der indeholder mellemrum, for at undgå fejl.
- `dirname` kan være nyttig i kombination med andre kommandoer som `basename` for at manipulere filstier effektivt.
- Overvej at bruge `dirname` i scripts til at gøre dem mere dynamiske og fleksible ved at udtrække stier fra variabler.