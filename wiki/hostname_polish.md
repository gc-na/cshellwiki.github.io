# [Linux] Bash hostname użycie: Wyświetlanie lub ustawianie nazwy hosta

## Overview
Polecenie `hostname` w systemie Linux służy do wyświetlania lub ustawiania nazwy hosta systemu. Nazwa hosta to unikalny identyfikator komputera w sieci, który umożliwia innym urządzeniom jego rozpoznanie.

## Usage
Podstawowa składnia polecenia `hostname` jest następująca:

```bash
hostname [opcje] [argumenty]
```

## Common Options
- `-a`, `--alias`: Wyświetla alias hosta.
- `-d`, `--domain`: Wyświetla nazwę domeny.
- `-f`, `--fqdn`: Wyświetla pełną nazwę kwalifikowaną (FQDN) hosta.
- `-i`, `--ip-address`: Wyświetla adres IP hosta.
- `-s`, `--short`: Wyświetla krótką nazwę hosta.

## Common Examples
1. Wyświetlenie aktualnej nazwy hosta:
   ```bash
   hostname
   ```

2. Ustawienie nowej nazwy hosta:
   ```bash
   sudo hostname nowa-nazwa-host
   ```

3. Wyświetlenie pełnej nazwy kwalifikowanej:
   ```bash
   hostname -f
   ```

4. Wyświetlenie adresu IP hosta:
   ```bash
   hostname -i
   ```

5. Wyświetlenie krótkiej nazwy hosta:
   ```bash
   hostname -s
   ```

## Tips
- Aby zmiany w nazwie hosta były trwałe po restarcie, należy zaktualizować odpowiedni plik konfiguracyjny, np. `/etc/hostname`.
- Używaj polecenia `hostname` z uprawnieniami administratora (np. `sudo`), gdy chcesz zmienić nazwę hosta.
- Regularnie sprawdzaj nazwę hosta, aby upewnić się, że jest zgodna z polityką nazewnictwa w Twojej sieci.