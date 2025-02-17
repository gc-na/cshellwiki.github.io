# [Linux] Bash cmp användning: Jämför två filer byte för byte

## Översikt
`cmp` är ett Bash-kommando som används för att jämföra två filer byte för byte. Det rapporterar den första skillnaden mellan filerna och kan vara användbart för att kontrollera om två filer är identiska eller för att identifiera specifika skillnader.

## Användning
Den grundläggande syntaxen för `cmp` är:

```bash
cmp [alternativ] [fil1] [fil2]
```

## Vanliga alternativ
- `-l`: Lista alla byte som skiljer sig mellan filerna.
- `-s`: Tyst läge, ingen utdata om filerna är lika.
- `-i OFFSET`: Starta jämförelsen vid det angivna byte-offsetet.
- `-n N`: Jämför endast de första N byte av filerna.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `cmp`:

1. Jämför två filer och visa den första skillnaden:
   ```bash
   cmp fil1.txt fil2.txt
   ```

2. Jämför två filer utan att visa något om de är lika:
   ```bash
   cmp -s fil1.txt fil2.txt
   ```

3. Lista alla skillnader mellan två filer:
   ```bash
   cmp -l fil1.txt fil2.txt
   ```

4. Jämför endast de första 10 byte av två filer:
   ```bash
   cmp -n 10 fil1.txt fil2.txt
   ```

5. Jämför filer med en specifik startpunkt:
   ```bash
   cmp -i 5 fil1.txt fil2.txt
   ```

## Tips
- Använd `cmp -s` för att snabbt kontrollera om två filer är identiska utan att få en massa utdata.
- Om du arbetar med stora filer och bara är intresserad av skillnader, använd `cmp -l` för att få en detaljerad lista över avvikelser.
- Tänk på att `cmp` är känsligt för filens innehåll och inte tar hänsyn till filens metadata, som tidpunkter för ändringar eller filstorlek.