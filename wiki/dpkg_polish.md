# [Linux] Bash dpkg Użycie: Zarządzanie pakietami w systemie Debian

## Overview
Polecenie `dpkg` jest narzędziem do zarządzania pakietami w systemach opartych na Debianie, takich jak Ubuntu. Umożliwia instalację, usuwanie i zarządzanie pakietami oprogramowania w formacie `.deb`.

## Usage
Podstawowa składnia polecenia `dpkg` jest następująca:

```
dpkg [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `dpkg`:

- `-i` : Instalacja pakietu.
- `-r` : Usunięcie pakietu.
- `-l` : Wyświetlenie listy zainstalowanych pakietów.
- `-s` : Wyświetlenie statusu pakietu.
- `-c` : Wyświetlenie zawartości pakietu.

## Common Examples

### Instalacja pakietu
Aby zainstalować pakiet `.deb`, użyj polecenia:

```bash
dpkg -i nazwa_pakietu.deb
```

### Usunięcie pakietu
Aby usunąć zainstalowany pakiet, użyj:

```bash
dpkg -r nazwa_pakietu
```

### Wyświetlenie listy zainstalowanych pakietów
Aby zobaczyć wszystkie zainstalowane pakiety, użyj:

```bash
dpkg -l
```

### Sprawdzenie statusu pakietu
Aby sprawdzić status konkretnego pakietu, użyj:

```bash
dpkg -s nazwa_pakietu
```

### Wyświetlenie zawartości pakietu
Aby zobaczyć, co znajduje się w pakiecie `.deb`, użyj:

```bash
dpkg -c nazwa_pakietu.deb
```

## Tips
- Zawsze sprawdzaj zależności pakietów przed ich instalacją, aby uniknąć problemów.
- Używaj `dpkg` w połączeniu z `apt` dla lepszej obsługi zależności.
- Regularnie aktualizuj listę pakietów, aby mieć dostęp do najnowszych wersji oprogramowania.