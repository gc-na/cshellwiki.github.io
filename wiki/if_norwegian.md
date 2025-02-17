# [Linux] Bash if bruken: Evaluere betingelser

## Oversikt
`if`-kommandoen i Bash brukes til å evaluere betingelser og utføre kommandoer basert på resultatet av disse betingelsene. Den lar deg kontrollere flyten av skript ved å sjekke om en bestemt tilstand er sann eller usann.

## Bruk
Grunnleggende syntaks for `if`-kommandoen er som følger:

```bash
if [ betingelse ]; then
    # kommandoer som skal utføres hvis betingelsen er sann
fi
```

## Vanlige alternativer
- `-e`: Sjekker om en fil eksisterer.
- `-d`: Sjekker om en fil er en katalog.
- `-f`: Sjekker om en fil er en vanlig fil.
- `-z`: Sjekker om lengden på en streng er null.
- `-n`: Sjekker om lengden på en streng ikke er null.

## Vanlige eksempler

### Eksempel 1: Sjekke om en fil eksisterer
```bash
if [ -e fil.txt ]; then
    echo "Fil eksisterer."
else
    echo "Fil finnes ikke."
fi
```

### Eksempel 2: Sjekke om en katalog eksisterer
```bash
if [ -d /path/to/katalog ]; then
    echo "Katalogen eksisterer."
else
    echo "Katalogen finnes ikke."
fi
```

### Eksempel 3: Sjekke om en variabel er tom
```bash
variabel=""
if [ -z "$variabel" ]; then
    echo "Variabelen er tom."
else
    echo "Variabelen har innhold."
fi
```

### Eksempel 4: Kombinere betingelser
```bash
if [ -f fil.txt ] && [ -r fil.txt ]; then
    echo "Fil eksisterer og er lesbar."
else
    echo "Fil eksisterer ikke eller er ikke lesbar."
fi
```

## Tips
- Husk å bruke mellomrom rundt `[` og `]` i betingelsene.
- For mer komplekse betingelser, vurder å bruke `elif` for å sjekke flere tilstander.
- Test alltid skriptene dine i et trygt miljø før du kjører dem i produksjon for å unngå utilsiktede konsekvenser.