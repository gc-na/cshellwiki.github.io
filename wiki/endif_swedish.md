# [Linux] Bash endif användning: Avsluta en if-sats

## Översikt
`endif` är en kommandon som används i Bash-skript för att avsluta en if-sats. Det är en del av den strukturella syntaxen för att definiera villkorlig logik i skript. `endif` används för att tydligt markera slutet på en if-sats, vilket gör koden mer läsbar och organiserad.

## Användning
Den grundläggande syntaxen för `endif` är inte en fristående kommando utan används i samband med `if`-satser. Här är ett exempel på hur det kan se ut i ett skript:

```bash
if [ condition ]; then
    # kommandon att köra om villkoret är sant
fi
```

Observera att `endif` inte är ett faktiskt kommando i Bash; istället används `fi` för att avsluta en if-sats.

## Vanliga alternativ
Eftersom `endif` inte är ett fristående kommando, finns det inga specifika alternativ för det. Men här är några vanliga alternativ för `if`-kommandot som kan användas tillsammans med `fi`:

- `-eq`: Jämför om två tal är lika.
- `-ne`: Jämför om två tal inte är lika.
- `-gt`: Jämför om ett tal är större än ett annat.
- `-lt`: Jämför om ett tal är mindre än ett annat.
- `-z`: Kontrollerar om en sträng är tom.

## Vanliga exempel
Här är några praktiska exempel på hur `if` och `fi` används i Bash-skript:

### Exempel 1: Enkel if-sats
```bash
if [ -f "fil.txt" ]; then
    echo "Filen finns."
fi
```

### Exempel 2: If-sats med else
```bash
if [ -d "mapp" ]; then
    echo "Mappen finns."
else
    echo "Mappen finns inte."
fi
```

### Exempel 3: If-sats med flera villkor
```bash
if [ -z "$variabel" ]; then
    echo "Variabeln är tom."
elif [ "$variabel" -eq 1 ]; then
    echo "Variabeln är 1."
else
    echo "Variabeln har ett annat värde."
fi
```

## Tips
- Se till att alltid avsluta dina if-satser med `fi` för att undvika syntaxfel.
- Använd indragning för att göra din kod mer läsbar, särskilt när du har flera nivåer av if-satser.
- Testa alltid dina skript för att säkerställa att logiken fungerar som förväntat, särskilt när du använder komplexa villkor.