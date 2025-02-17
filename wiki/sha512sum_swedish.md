# [Linux] Bash sha512sum användning: Beräkna SHA-512 hashvärden

## Översikt
Kommandot `sha512sum` används för att beräkna och verifiera SHA-512 hashvärden för filer. Det är ett viktigt verktyg för att säkerställa dataintegritet och kan användas för att skapa digitala signaturer.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
sha512sum [alternativ] [argument]
```

## Vanliga alternativ
- `-b`, `--binary`: Behandla filen som binär.
- `-c`, `--check`: Kontrollera hashvärden mot en given fil.
- `-h`, `--help`: Visa hjälpinformation om kommandot.
- `-t`, `--text`: Behandla filen som text (standard).

## Vanliga exempel

### Beräkna SHA-512 hashvärde för en fil
För att beräkna hashvärdet för en fil, använd följande kommando:

```bash
sha512sum fil.txt
```

### Spara hashvärdet i en fil
För att spara hashvärdet i en fil kan du omdirigera utdata:

```bash
sha512sum fil.txt > hash.txt
```

### Kontrollera hashvärden
För att kontrollera hashvärden mot en lista i en fil, använd:

```bash
sha512sum -c hash.txt
```

### Beräkna hashvärde för flera filer
Du kan beräkna hashvärden för flera filer samtidigt:

```bash
sha512sum fil1.txt fil2.txt fil3.txt
```

## Tips
- Använd `-c` alternativet för att verifiera integriteten hos filer efter överföring.
- Det är en bra praxis att alltid spara hashvärden när du laddar ner viktiga filer för att kunna kontrollera dem senare.
- Tänk på att hashvärden är känsliga för även de minsta ändringar i filinnehållet, så se till att filerna inte ändras efter att hashvärdet har beräknats.