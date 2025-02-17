# [Linux] Bash script användning: Spela in terminalsessioner

## Översikt
Kommandot `script` används för att spela in en terminalsession. Det skapar en fil som innehåller allt som skrivs ut på skärmen under sessionen, vilket är användbart för att dokumentera kommandon och deras utdata.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
script [alternativ] [filnamn]
```

## Vanliga alternativ
- `-a`: Lägg till utdata till en befintlig fil istället för att skriva över den.
- `-c`: Kör ett kommando och spela in dess utdata.
- `-f`: Skriver ut utdata till terminalen i realtid.
- `-q`: Tyst läge, ingen information om sessionen skrivs ut.

## Vanliga exempel
### Spela in en session
För att spela in en session till en fil som heter `session.log`, kör:

```bash
script session.log
```

### Spela in och köra ett kommando
För att spela in utdata av ett specifikt kommando, som `ls`, använd:

```bash
script -c "ls" output.log
```

### Lägg till utdata till en befintlig fil
För att lägga till en ny session till en redan existerande fil, använd:

```bash
script -a session.log
```

### Spela in med realtidsutskrift
För att spela in en session och se utdata i realtid, använd:

```bash
script -f session.log
```

## Tips
- Använd `exit` för att avsluta inspelningen av sessionen.
- Kontrollera filens innehåll med `cat` eller `less` efter att du har avslutat inspelningen för att se vad som har spelats in.
- Tänk på att inspelningen kan innehålla känslig information, så hantera filerna med försiktighet.