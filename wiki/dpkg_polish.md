# [Linux] C Shell (csh) dpkg użycie: zarządzanie pakietami w systemie Debian

## Overview
Polecenie `dpkg` jest narzędziem do zarządzania pakietami w systemach opartych na Debianie. Umożliwia instalację, usuwanie oraz zarządzanie pakietami oprogramowania w formacie `.deb`.

## Usage
Podstawowa składnia polecenia `dpkg` jest następująca:

```
dpkg [opcje] [argumenty]
```

## Common Options
- `-i` : Instalacja pakietu.
- `-r` : Usunięcie pakietu.
- `-l` : Wyświetlenie listy zainstalowanych pakietów.
- `-s` : Wyświetlenie statusu pakietu.
- `-c` : Wyświetlenie zawartości pakietu.

## Common Examples
- Instalacja pakietu:
  ```bash
  dpkg -i nazwa_pakietu.deb
  ```

- Usunięcie pakietu:
  ```bash
  dpkg -r nazwa_pakietu
  ```

- Wyświetlenie listy zainstalowanych pakietów:
  ```bash
  dpkg -l
  ```

- Sprawdzenie statusu pakietu:
  ```bash
  dpkg -s nazwa_pakietu
  ```

- Wyświetlenie zawartości pakietu:
  ```bash
  dpkg -c nazwa_pakietu.deb
  ```

## Tips
- Zawsze sprawdzaj zależności pakietów przed ich instalacją, aby uniknąć problemów z brakującymi bibliotekami.
- Używaj opcji `-l` regularnie, aby mieć przegląd zainstalowanych pakietów.
- W przypadku problemów z instalacją, sprawdź logi systemowe, aby zidentyfikować przyczynę.