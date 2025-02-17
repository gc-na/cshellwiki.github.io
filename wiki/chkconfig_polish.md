# [Linux] Bash chkconfig użycie: Zarządzanie usługami systemowymi

## Overview
Polecenie `chkconfig` jest używane do zarządzania usługami systemowymi w systemach Linux, które korzystają z systemu init. Umożliwia włączanie, wyłączanie oraz sprawdzanie statusu usług, co jest kluczowe dla zarządzania działaniem systemu operacyjnego.

## Usage
Podstawowa składnia polecenia `chkconfig` jest następująca:

```bash
chkconfig [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `chkconfig`:

- `--list` - Wyświetla wszystkie usługi oraz ich status (włączone/wyłączone) dla różnych poziomów uruchamiania.
- `--add <usługa>` - Dodaje nową usługę do zarządzania przez `chkconfig`.
- `--del <usługa>` - Usuwa usługę z zarządzania przez `chkconfig`.
- `--level <poziom>` - Określa poziom uruchamiania, dla którego ma być zastosowana operacja (np. 2, 3, 4, 5).

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `chkconfig`:

1. **Wyświetlenie statusu wszystkich usług:**
   ```bash
   chkconfig --list
   ```

2. **Włączenie usługi:**
   ```bash
   chkconfig httpd on
   ```

3. **Wyłączenie usługi:**
   ```bash
   chkconfig httpd off
   ```

4. **Dodanie nowej usługi:**
   ```bash
   chkconfig --add myservice
   ```

5. **Usunięcie usługi:**
   ```bash
   chkconfig --del myservice
   ```

## Tips
- Zawsze sprawdzaj status usług po ich włączeniu lub wyłączeniu, aby upewnić się, że działają zgodnie z oczekiwaniami.
- Używaj opcji `--level`, aby precyzyjnie określić, na jakim poziomie uruchamiania ma być aktywna usługa.
- Regularnie przeglądaj listę usług, aby zarządzać nimi efektywnie i unikać niepotrzebnych obciążeń systemu.