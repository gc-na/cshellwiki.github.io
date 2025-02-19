# [Linux] C Shell (csh) docker-compose użycie: Zarządzanie aplikacjami w kontenerach

## Overview
`docker-compose` to narzędzie, które pozwala na definiowanie i uruchamianie aplikacji składających się z wielu kontenerów Docker. Dzięki plikowi konfiguracyjnemu `docker-compose.yml`, użytkownicy mogą łatwo zarządzać usługami, sieciami i wolumenami, które są częścią ich aplikacji.

## Usage
Podstawowa składnia polecenia `docker-compose` jest następująca:

```bash
docker-compose [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `docker-compose`:

- `up`: Uruchamia kontenery zdefiniowane w pliku `docker-compose.yml`.
- `down`: Zatrzymuje i usuwa kontenery, sieci i wolumeny utworzone przez `up`.
- `build`: Buduje obrazy kontenerów zgodnie z definicjami w pliku `docker-compose.yml`.
- `logs`: Wyświetla logi kontenerów.
- `ps`: Wyświetla status uruchomionych kontenerów.

## Common Examples
Oto kilka praktycznych przykładów użycia `docker-compose`:

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

4. **Budowanie obrazów kontenerów**:
   ```bash
   docker-compose build
   ```

5. **Wyświetlanie logów kontenerów**:
   ```bash
   docker-compose logs
   ```

## Tips
- Używaj opcji `-d` (detached mode), aby uruchomić kontenery w tle, co pozwala na dalszą pracę w terminalu.
- Regularnie przeglądaj logi kontenerów, aby monitorować ich działanie i szybko wykrywać problemy.
- Zawsze sprawdzaj plik `docker-compose.yml` pod kątem błędów przed uruchomieniem polecenia `up`, aby uniknąć problemów z konfiguracją.