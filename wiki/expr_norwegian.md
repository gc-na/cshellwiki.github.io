# [Linux] Bash expr Bruk: Utfør evaluering av uttrykk

## Oversikt
`expr` er et kommandolinjeverktøy i Bash som brukes til å evaluere uttrykk og utføre enkle matematiske operasjoner, sammenligninger og tekstmanipulasjon. Det er nyttig for skripting og automatisering av oppgaver.

## Bruk
Grunnleggende syntaks for `expr` er som følger:

```bash
expr [alternativer] [argumenter]
```

## Vanlige alternativer
- `+` : Legger sammen to tall.
- `-` : Trekker det andre tallet fra det første.
- `*` : Multipliserer to tall (bruk `\*` for å unngå at det tolkes som et jokertegn).
- `/` : Deler det første tallet med det andre.
- `%` : Returnerer resten av divisjonen.
- `=` : Sjekker om to verdier er like.
- `!=` : Sjekker om to verdier ikke er like.
- `<` : Sjekker om det første tallet er mindre enn det andre.
- `>` : Sjekker om det første tallet er større enn det andre.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `expr`:

### 1. Legge sammen to tall
```bash
expr 5 + 3
```
Output: `8`

### 2. Trekke fra to tall
```bash
expr 10 - 4
```
Output: `6`

### 3. Multiplisere to tall
```bash
expr 7 \* 6
```
Output: `42`

### 4. Dele to tall
```bash
expr 20 / 4
```
Output: `5`

### 5. Sjekke om to tall er like
```bash
expr 5 = 5
```
Output: `1` (sann)

### 6. Sjekke om et tall er mindre enn et annet
```bash
expr 3 \< 5
```
Output: `1` (sann)

## Tips
- Husk å bruke escape-tegn (`\`) foran `*` for å unngå at det tolkes som et jokertegn.
- `expr` returnerer `0` for falske betingelser og `1` for sanne betingelser, noe som kan være nyttig i skript.
- For mer komplekse matematiske operasjoner, vurder å bruke `bc` eller `$((...))` syntaksen i Bash, som gir mer fleksibilitet.