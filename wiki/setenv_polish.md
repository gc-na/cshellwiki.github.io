# [Linux] Bash setenv Użycie: Ustawianie zmiennych środowiskowych

## Overview
Polecenie `setenv` służy do ustawiania zmiennych środowiskowych w powłoce Bash. Umożliwia użytkownikom definiowanie i modyfikowanie zmiennych, które mogą być używane przez różne procesy i aplikacje w systemie.

## Usage
Podstawowa składnia polecenia `setenv` jest następująca:

```bash
setenv [nazwa_zmiennej] [wartość]
```

## Common Options
Polecenie `setenv` nie ma wielu opcji, ponieważ jego główną funkcją jest ustawianie zmiennych. Oto kilka przykładów:

- `nazwa_zmiennej`: Nazwa zmiennej, którą chcesz ustawić.
- `wartość`: Wartość, którą chcesz przypisać do zmiennej.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `setenv`:

1. Ustawienie zmiennej `PATH`:
   ```bash
   setenv PATH /usr/local/bin:$PATH
   ```

2. Ustawienie zmiennej `JAVA_HOME`:
   ```bash
   setenv JAVA_HOME /usr/lib/jvm/java-11-openjdk-amd64
   ```

3. Ustawienie zmiennej `EDITOR`:
   ```bash
   setenv EDITOR nano
   ```

4. Ustawienie zmiennej `MY_VAR` na wartość `Hello World`:
   ```bash
   setenv MY_VAR "Hello World"
   ```

## Tips
- Używaj `setenv` w skryptach startowych, aby automatycznie ustawiać zmienne środowiskowe przy uruchamianiu powłoki.
- Pamiętaj, że zmienne ustawione za pomocą `setenv` będą dostępne tylko w bieżącej sesji powłoki. Aby były trwałe, dodaj je do pliku konfiguracyjnego, takiego jak `.bashrc` lub `.bash_profile`.
- Używaj cudzysłowów dla wartości zawierających spacje, aby uniknąć błędów.