# [Linux] Bash rehash użycie: Odświeżanie ścieżek do poleceń

## Overview
Polecenie `rehash` w Bash jest używane do odświeżania pamięci podręcznej poleceń. Kiedy dodajesz nowe polecenia lub zmieniasz istniejące w katalogach, `rehash` pozwala na aktualizację listy dostępnych poleceń, co umożliwia ich natychmiastowe użycie bez konieczności ponownego uruchamiania powłoki.

## Usage
Podstawowa składnia polecenia `rehash` jest następująca:

```bash
rehash [options] [arguments]
```

## Common Options
- `-p`: Użyj tej opcji, aby zaktualizować tylko pamięć podręczną dla poleceń w katalogach znajdujących się w zmiennej środowiskowej `PATH`.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `rehash`:

1. **Podstawowe użycie rehash**:
   ```bash
   rehash
   ```

2. **Odświeżenie pamięci podręcznej poleceń w katalogach PATH**:
   ```bash
   rehash -p
   ```

3. **Dodanie nowego polecenia i odświeżenie pamięci podręcznej**:
   Załóżmy, że dodałeś nowy skrypt do katalogu `/usr/local/bin`, aby go użyć, wystarczy wywołać:
   ```bash
   rehash
   ```

## Tips
- Używaj `rehash` po dodaniu nowych skryptów do katalogów, aby upewnić się, że są one dostępne w bieżącej sesji powłoki.
- Jeśli często zmieniasz polecenia, rozważ dodanie `rehash` do swojego skryptu startowego, aby automatycznie aktualizować pamięć podręczną przy każdym uruchomieniu powłoki.
- Pamiętaj, że `rehash` działa tylko w powłoce, która obsługuje to polecenie, jak `csh` lub `tcsh`. W Bash nie jest to konieczne, ponieważ Bash automatycznie aktualizuje pamięć podręczną poleceń.