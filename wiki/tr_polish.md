# [Linux] C Shell (csh) tr <Użycie>: zamiana znaków

## Overview
Polecenie `tr` w C Shell (csh) służy do tłumaczenia lub usuwania znaków z wejścia. Umożliwia zamianę jednych znaków na inne, co jest przydatne w wielu scenariuszach, takich jak przetwarzanie tekstu czy formatowanie danych.

## Usage
Podstawowa składnia polecenia `tr` jest następująca:

```csh
tr [opcje] [argumenty]
```

## Common Options
- `-d`: Usuwa wskazane znaki z wejścia.
- `-s`: Zmniejsza powtarzające się znaki do jednego wystąpienia.
- `-c`: Wskazuje dozwolone znaki do zamiany, a wszystkie inne są ignorowane.

## Common Examples
1. **Zamiana małych liter na wielkie:**
   ```csh
   echo "hello world" | tr 'a-z' 'A-Z'
   ```
   Wynik: `HELLO WORLD`

2. **Usuwanie cyfr z tekstu:**
   ```csh
   echo "abc123def456" | tr -d '0-9'
   ```
   Wynik: `abcdef`

3. **Zamiana spacji na znaki podkreślenia:**
   ```csh
   echo "Hello World" | tr ' ' '_'
   ```
   Wynik: `Hello_World`

4. **Zmniejszanie powtarzających się spacji:**
   ```csh
   echo "This    is  a test" | tr -s ' '
   ```
   Wynik: `This is a test`

## Tips
- Używaj opcji `-d`, aby szybko usunąć niechciane znaki z danych wejściowych.
- Pamiętaj, że `tr` działa tylko na pojedynczych znakach, więc nie używaj go do zamiany całych słów.
- Możesz łączyć `tr` z innymi poleceniami w potokach, aby zwiększyć jego funkcjonalność.