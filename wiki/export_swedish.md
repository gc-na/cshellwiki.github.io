# [Linux] Bash export användning: Hantera miljövariabler

## Översikt
Kommandot `export` används i Bash för att skapa eller ändra miljövariabler, vilket gör dem tillgängliga för alla underprocesser som startas från den aktuella shell-sessionen. Detta är särskilt användbart när du vill att vissa inställningar eller värden ska vara tillgängliga för program och skript som körs i samma miljö.

## Användning
Den grundläggande syntaxen för kommandot `export` är:

```bash
export [alternativ] [argument]
```

## Vanliga alternativ
- `-n`: Ta bort exportstatusen för en variabel, vilket gör den lokal för den aktuella shell-sessionen.
- `-p`: Visa alla exporterade variabler och deras värden.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `export`:

### Exempel 1: Exportera en variabel
För att skapa och exportera en variabel kan du använda följande kommando:

```bash
export MY_VAR="Hej världen"
```

### Exempel 2: Kontrollera exporterade variabler
För att se alla exporterade variabler kan du använda:

```bash
export -p
```

### Exempel 3: Ta bort exportstatusen för en variabel
Om du vill göra en tidigare exporterad variabel lokal kan du köra:

```bash
export -n MY_VAR
```

### Exempel 4: Använda en exporterad variabel i ett skript
Om du har exporterat en variabel kan du använda den i ett skript:

```bash
#!/bin/bash
export MY_VAR="Värde"
bash -c 'echo $MY_VAR'
```

## Tips
- Använd `export` för att säkerställa att viktiga variabler är tillgängliga för alla skript och program som körs från din shell-session.
- Var försiktig med att exportera känsliga data, som lösenord, eftersom de kan bli tillgängliga för andra processer.
- Om du ofta använder samma miljövariabler, överväg att lägga till dem i din `~/.bashrc`-fil för att automatiskt exportera dem vid varje inloggning.