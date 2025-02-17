# [Linux] Bash mkdir användning: Skapa kataloger

## Översikt
`mkdir` (make directory) är ett Bash-kommando som används för att skapa nya kataloger i filsystemet. Det är ett grundläggande verktyg för att organisera filer och mappar.

## Användning
Den grundläggande syntaxen för `mkdir` är:

```bash
mkdir [alternativ] [argument]
```

## Vanliga alternativ
- `-p`: Skapar föräldrakataloger om de inte redan finns.
- `-v`: Visar detaljerad information om vad som skapas.
- `-m`: Sätter rättigheterna för den skapade katalogen.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mkdir`:

1. Skapa en enkel katalog:
    ```bash
    mkdir minKatalog
    ```

2. Skapa flera kataloger samtidigt:
    ```bash
    mkdir katalog1 katalog2 katalog3
    ```

3. Skapa en katalog med föräldrakataloger:
    ```bash
    mkdir -p /hem/användare/projekt
    ```

4. Skapa en katalog och visa information om skapandet:
    ```bash
    mkdir -v nyKatalog
    ```

5. Skapa en katalog med specifika rättigheter:
    ```bash
    mkdir -m 755 skyddadKatalog
    ```

## Tips
- Använd `-p` alternativet för att undvika fel när du försöker skapa en katalog i en väg där föräldrakatalogerna kanske inte finns.
- Kontrollera alltid rättigheterna för en katalog efter skapandet, särskilt om den ska delas med andra användare.
- Använd `-v` för att få bekräftelse på att katalogerna skapades som förväntat, vilket kan vara användbart i skript.