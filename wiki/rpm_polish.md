# [Linux] Bash rpm użycie: Zarządzanie pakietami RPM

## Overview
Polecenie `rpm` jest narzędziem do zarządzania pakietami w systemach operacyjnych opartych na Red Hat, takich jak Fedora, CentOS czy RHEL. Umożliwia instalację, usuwanie, aktualizację oraz sprawdzanie pakietów w formacie RPM.

## Usage
Podstawowa składnia polecenia `rpm` wygląda następująco:

```bash
rpm [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `rpm`:

- `-i` : Instalacja nowego pakietu.
- `-e` : Usunięcie zainstalowanego pakietu.
- `-U` : Aktualizacja zainstalowanego pakietu do nowszej wersji.
- `-q` : Zapytanie o zainstalowane pakiety.
- `-V` : Weryfikacja zainstalowanego pakietu.
- `--help` : Wyświetlenie pomocy dotyczącej użycia polecenia.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `rpm`:

1. **Instalacja pakietu:**
   ```bash
   rpm -i nazwa_pakietu.rpm
   ```

2. **Usunięcie pakietu:**
   ```bash
   rpm -e nazwa_pakietu
   ```

3. **Aktualizacja pakietu:**
   ```bash
   rpm -U nazwa_pakietu.rpm
   ```

4. **Sprawdzenie, czy pakiet jest zainstalowany:**
   ```bash
   rpm -q nazwa_pakietu
   ```

5. **Weryfikacja pakietu:**
   ```bash
   rpm -V nazwa_pakietu
   ```

## Tips
- Zawsze sprawdzaj zależności przed instalacją pakietu, aby uniknąć problemów.
- Używaj opcji `-q` z dodatkowymi parametrami, aby uzyskać więcej informacji o zainstalowanych pakietach.
- Regularnie aktualizuj swoje pakiety, aby zapewnić bezpieczeństwo i stabilność systemu.