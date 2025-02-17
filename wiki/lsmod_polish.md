# [Linux] Bash lsmod użycie: wyświetlanie załadowanych modułów jądra

## Przegląd
Polecenie `lsmod` jest używane w systemach Linux do wyświetlania listy aktualnie załadowanych modułów jądra. Moduły jądra to fragmenty kodu, które mogą być dynamicznie ładowane i odładowywane w trakcie działania systemu, co pozwala na rozszerzenie jego funkcjonalności.

## Użycie
Podstawowa składnia polecenia `lsmod` jest następująca:

```bash
lsmod [opcje]
```

## Częste opcje
`lsmod` nie posiada wielu opcji, ale oto kilka, które mogą być przydatne:

- **-h, --help**: Wyświetla pomoc dotyczącą użycia polecenia.
- **-q, --quiet**: Wyłącza wyjście informacji o błędach.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `lsmod`:

1. **Wyświetlenie listy załadowanych modułów:**

   ```bash
   lsmod
   ```

2. **Wyświetlenie pomocy:**

   ```bash
   lsmod --help
   ```

3. **Cisza w wyjściu (jeśli występują błędy):**

   ```bash
   lsmod --quiet
   ```

## Wskazówki
- Użyj `lsmod` w połączeniu z innymi poleceniami, takimi jak `grep`, aby filtrować wyniki. Na przykład, aby znaleźć moduł o nazwie "nvidia", użyj:
  
  ```bash
  lsmod | grep nvidia
  ```

- Regularne sprawdzanie załadowanych modułów może pomóc w diagnozowaniu problemów z urządzeniami i sterownikami.

- Pamiętaj, że `lsmod` wyświetla tylko moduły, które są aktualnie załadowane. Aby załadować lub odładować moduł, użyj poleceń `modprobe` lub `rmmod`.