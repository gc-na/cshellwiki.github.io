# [Linux] C Shell (csh) chkconfig użycie: Zarządzanie usługami systemowymi

## Przegląd
Polecenie `chkconfig` służy do zarządzania usługami systemowymi w systemach opartych na Linuxie. Umożliwia użytkownikowi włączanie, wyłączanie oraz sprawdzanie statusu usług, co jest szczególnie przydatne w kontekście zarządzania procesami uruchamianymi przy starcie systemu.

## Użycie
Podstawowa składnia polecenia `chkconfig` jest następująca:

```bash
chkconfig [opcje] [argumenty]
```

## Częste opcje
- `--list` - wyświetla wszystkie usługi oraz ich status (włączone/wyłączone).
- `--add` - dodaje nową usługę do zarządzania przez chkconfig.
- `--del` - usuwa usługę z zarządzania przez chkconfig.
- `--level` - określa poziomy uruchamiania, w których usługa ma być włączona lub wyłączona.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `chkconfig`:

1. **Wyświetlenie statusu wszystkich usług:**
   ```bash
   chkconfig --list
   ```

2. **Włączenie usługi przy starcie systemu:**
   ```bash
   chkconfig httpd on
   ```

3. **Wyłączenie usługi przy starcie systemu:**
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

## Wskazówki
- Zawsze sprawdzaj status usług po ich włączeniu lub wyłączeniu, aby upewnić się, że działają zgodnie z oczekiwaniami.
- Używaj opcji `--level`, aby precyzyjnie określić, w których runlevelach ma być aktywna dana usługa.
- Regularnie przeglądaj listę usług, aby zarządzać nimi efektywnie i unikać niepotrzebnych obciążeń systemu.