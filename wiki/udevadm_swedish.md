# [Linux] Bash udevadm användning: Hantera enheter i Linux

## Översikt
`udevadm` är ett kommandoradsverktyg som används för att interagera med udev, en enhetshanterare för Linux. Det används för att hantera enheter och deras egenskaper, samt för att övervaka och kontrollera enhetsregistreringar.

## Användning
Den grundläggande syntaxen för `udevadm` är:

```bash
udevadm [alternativ] [argument]
```

## Vanliga alternativ
- `info`: Visar information om en specifik enhet.
- `trigger`: Utlöser udev-händelser för enheter.
- `settle`: Väntar på att alla udev-händelser ska slutföras.
- `control`: Kontrollerar udev:s beteende, till exempel om det ska köras i bakgrunden.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `udevadm`:

### Visa information om en enhet
För att visa information om en specifik enhet, använd följande kommando:

```bash
udevadm info --query=all --name=/dev/sda
```

### Utlösa udev-händelser
För att utlösa udev-händelser för alla enheter kan du använda:

```bash
udevadm trigger
```

### Vänta på att udev-händelser ska slutföras
För att vänta på att alla udev-händelser ska slutföras, kör:

```bash
udevadm settle
```

### Kontrollera udev:s beteende
För att kontrollera om udev körs i bakgrunden, använd:

```bash
udevadm control --reload-rules
```

## Tips
- Använd `udevadm info` för att få detaljerad information om enheter när du felsöker enhetsproblem.
- Var försiktig med `udevadm trigger`, eftersom det kan påverka systemets stabilitet om det används felaktigt.
- Kontrollera alltid udev-reglerna efter att ha gjort ändringar för att säkerställa att de tillämpas korrekt.