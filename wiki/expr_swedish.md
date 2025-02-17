# [Linux] Bash expr användning: Utför beräkningar och strängoperationer

## Översikt
`expr` är ett kommandoradsverktyg i Bash som används för att utföra grundläggande matematiska beräkningar och strängoperationer. Det kan hantera aritmetiska operationer, jämförelser och strängmanipulationer.

## Användning
Den grundläggande syntaxen för `expr` är:

```bash
expr [alternativ] [argument]
```

## Vanliga alternativ
- `+` : Addition av två tal.
- `-` : Subtraktion av två tal.
- `*` : Multiplikation av två tal (notera att `*` måste omges av citattecken eller backslash).
- `/` : Division av två tal.
- `%` : Modulus, ger resten av divisionen.
- `=` : Jämförelse för att kontrollera om två värden är lika.
- `!=` : Jämförelse för att kontrollera om två värden inte är lika.
- `>` : Jämförelse för att kontrollera om vänster värde är större än höger.
- `<` : Jämförelse för att kontrollera om vänster värde är mindre än höger.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `expr`:

### Aritmetiska operationer
Addition av två tal:
```bash
expr 5 + 3
```

Subtraktion av två tal:
```bash
expr 10 - 4
```

Multiplikation av två tal:
```bash
expr 6 \* 7
```

Division av två tal:
```bash
expr 20 / 4
```

Modulus:
```bash
expr 10 % 3
```

### Jämförelser
Kontrollera om två tal är lika:
```bash
expr 5 = 5
```

Kontrollera om ett tal är större än ett annat:
```bash
expr 10 \> 5
```

### Strängoperationer
Beräkna längden på en sträng:
```bash
expr length "Hej världen"
```

Hämta en del av en sträng:
```bash
expr substr "Bash scripting" 1 4
```

## Tips
- Använd alltid backslash (`\`) före `*` för att undvika att det tolkas som en jokertecken.
- Om du arbetar med strängar, se till att använda citattecken för att undvika problem med mellanslag.
- Tänk på att `expr` returnerar ett värde som kan användas i andra kommandon, så du kan kombinera det med andra Bash-funktioner för mer komplexa operationer.