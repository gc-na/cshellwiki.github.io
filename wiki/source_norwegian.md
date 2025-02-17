# [Linux] Bash source bruk: Kjøring av skript i gjeldende skall

## Oversikt
Kommandoen `source` brukes i Bash for å kjøre et skript i det nåværende skallmiljøet. Dette betyr at eventuelle variabler eller funksjoner som defineres i skriptet, vil være tilgjengelige etter at skriptet er kjørt. Dette er nyttig for å laste inn konfigurasjoner eller funksjoner uten å starte et nytt skall.

## Bruk
Den grunnleggende syntaksen for `source`-kommandoen er som følger:

```bash
source [alternativer] [argumenter]
```

## Vanlige alternativer
- `-`: Brukes for å spesifisere at skriptet skal kjøres i det nåværende skallmiljøet (dette er standard oppførsel).
- `.`: En kortform for `source`, som også kan brukes for å kjøre skriptet i det nåværende miljøet.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `source`-kommandoen:

### Laste inn en konfigurasjonsfil
For å laste inn en konfigurasjonsfil som setter opp miljøvariabler, kan du bruke:

```bash
source ~/.bashrc
```

### Kjøring av et skript
Hvis du har et skript som definerer funksjoner, kan du kjøre det slik:

```bash
source my_script.sh
```

### Bruke den korte formen
Du kan også bruke den korte formen for `source`:

```bash
. my_script.sh
```

## Tips
- Bruk `source` for å oppdatere miljøvariabler uten å måtte åpne et nytt skall.
- Sørg for at skriptet har de nødvendige tillatelsene for å bli kjørt.
- Hvis du har flere skript som må lastes inn, kan du lage en hovedkonfigurasjonsfil som kaller de andre skriptene med `source`.