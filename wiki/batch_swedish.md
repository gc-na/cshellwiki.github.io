# [Linux] Bash batch användning: Schemalägg kommandon för senare körning

## Översikt
Batch-kommandot används för att schemalägga kommandon eller skript så att de körs vid en senare tidpunkt, vanligtvis när systemet har låg belastning. Det är ett användbart verktyg för att hantera uppgifter som inte behöver köras omedelbart.

## Användning
Den grundläggande syntaxen för batch-kommandot är:

```bash
batch [alternativ] [argument]
```

## Vanliga alternativ
- `-l` : Specificera en lista över kommandon som ska köras.
- `-n` : Ange antalet gånger kommandot ska köras.
- `-q` : Tyst läge, ingen utdata till terminalen.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda batch-kommandot:

### Exempel 1: Schemalägg ett enkelt kommando
För att schemalägga ett kommando som ska köras senare, skriv:

```bash
echo "Uppgift som ska köras" | batch
```

### Exempel 2: Schemalägg flera kommandon
Du kan också schemalägga flera kommandon genom att använda en lista:

```bash
echo -e "kommand1\nkommand2\nkommand3" | batch
```

### Exempel 3: Använda batch med skript
Om du har ett skript som du vill köra senare, kan du göra så här:

```bash
echo "/path/to/your/script.sh" | batch
```

## Tips
- Kontrollera systemets belastning innan du schemalägger uppgifter för att säkerställa att de körs effektivt.
- Använd `at`-kommandot om du behöver mer kontroll över när ett kommando ska köras.
- Håll koll på batch-jobb genom att använda kommandot `atq` för att se en lista över schemalagda jobb.