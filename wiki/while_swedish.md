# [Linux] Bash while användning: Loopar genom kommandon

## Översikt
`while`-kommandot i Bash används för att skapa en loop som fortsätter att köra ett kommando eller en serie kommandon så länge ett angivet villkor är sant. Detta är användbart för att repetera uppgifter tills ett specifikt tillstånd uppnås.

## Användning
Den grundläggande syntaxen för `while`-kommandot är:

```bash
while [villkor ]; do
    # kommandon som ska köras
done
```

## Vanliga alternativ
`while`-kommandot har inga specifika alternativ, men villkoren som används kan vara olika typer av test, såsom:

- `true`: alltid sant, vilket skapar en oändlig loop.
- `false`: alltid falskt, vilket gör att loopen aldrig körs.
- `test -e fil`: kontrollerar om en fil existerar.

## Vanliga exempel

### Exempel 1: Enkel oändlig loop
```bash
while true; do
    echo "Detta kommer att köras för alltid."
done
```

### Exempel 2: Loopa tills en fil existerar
```bash
while [ ! -e "minfil.txt" ]; do
    echo "Väntar på att minfil.txt ska skapas..."
    sleep 1
done
echo "Fil hittades!"
```

### Exempel 3: Räkna ner
```bash
counter=5
while [ $counter -gt 0 ]; do
    echo "Räknar ner: $counter"
    ((counter--))
done
echo "Ner till noll!"
```

## Tips
- Var försiktig med oändliga loopar; se till att det finns ett villkor som så småningom blir falskt.
- Använd `sleep` för att undvika att loopen körs för snabbt och belastar systemet.
- Testa alltid villkoren noggrant för att säkerställa att de fungerar som förväntat.