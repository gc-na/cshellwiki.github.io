# [Linux] Bash docker-compose użycie: Zarządzanie aplikacjami kontenerowymi

## Przegląd
`docker-compose` to narzędzie, które umożliwia definiowanie i uruchamianie aplikacji wielokontenerowych w Dockerze. Umożliwia łatwe zarządzanie konfiguracjami kontenerów w pliku YAML, co upraszcza proces uruchamiania i skalowania aplikacji.

## Użycie
Podstawowa składnia polecenia `docker-compose` jest następująca:

```bash
docker-compose [opcje] [argumenty]
```

## Częste opcje
- `up` - Uruchamia kontenery zdefiniowane w pliku `docker-compose.yml`.
- `down` - Zatrzymuje i usuwa kontenery, sieci i wolumeny utworzone przez `up`.
- `build` - Buduje obrazy kontenerów zgodnie z definicjami w pliku.
- `logs` - Wyświetla logi kontenerów.
- `exec` - Wykonuje polecenie w działającym kontenerze.

## Częste przykłady
1. **Uruchomienie aplikacji**:
   ```bash
   docker-compose up
   ```

2. **Uruchomienie aplikacji w tle**:
   ```bash
   docker-compose up -d
   ```

3. **Zatrzymanie i usunięcie kontenerów**:
   ```bash
   docker-compose down
   ```

4. **Budowanie obrazów**:
   ```bash
   docker-compose build
   ```

5. **Wyświetlanie logów kontenerów**:
   ```bash
   docker-compose logs
   ```

6. **Wykonanie polecenia w kontenerze**:
   ```bash
   docker-compose exec <nazwa_kontenera> <polecenie>
   ```

## Wskazówki
- Używaj pliku `docker-compose.yml` do zarządzania konfiguracjami kontenerów, aby uprościć proces uruchamiania.
- Regularnie korzystaj z opcji `logs`, aby monitorować działanie aplikacji i diagnozować problemy.
- Zawsze testuj zmiany w lokalnym środowisku przed wdrożeniem na produkcję, aby uniknąć nieprzewidzianych problemów.