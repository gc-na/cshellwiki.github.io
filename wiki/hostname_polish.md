# [Linux] C Shell (csh) hostname użycie: Wyświetlanie lub ustawianie nazwy hosta

## Overview
Polecenie `hostname` w C Shell (csh) służy do wyświetlania lub ustawiania nazwy hosta systemu. Nazwa hosta to unikalny identyfikator, który pozwala na rozróżnienie urządzeń w sieci.

## Usage
Podstawowa składnia polecenia `hostname` jest następująca:

```
hostname [opcje] [argumenty]
```

## Common Options
- `-f` – Wyświetla pełną nazwę hosta (FQDN).
- `-s` – Wyświetla tylko krótką nazwę hosta.
- `-i` – Wyświetla adres IP przypisany do hosta.
- `-V` – Wyświetla wersję polecenia.

## Common Examples
- Aby wyświetlić aktualną nazwę hosta:
  ```csh
  hostname
  ```

- Aby ustawić nową nazwę hosta:
  ```csh
  hostname nowa_nazwa
  ```

- Aby wyświetlić pełną nazwę hosta:
  ```csh
  hostname -f
  ```

- Aby wyświetlić tylko krótką nazwę hosta:
  ```csh
  hostname -s
  ```

- Aby wyświetlić adres IP hosta:
  ```csh
  hostname -i
  ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia, aby zmieniać nazwę hosta, ponieważ może to wymagać uprawnień administratora.
- Po zmianie nazwy hosta, rozważ zaktualizowanie pliku `/etc/hosts`, aby odzwierciedlić nową nazwę.
- Sprawdź, czy nowa nazwa hosta jest poprawnie rozpoznawana w sieci, używając polecenia `ping`.