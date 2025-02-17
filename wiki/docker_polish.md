# [Linux] Bash docker użycie: Zarządzanie kontenerami aplikacji

## Overview
Polecenie `docker` jest narzędziem do zarządzania kontenerami aplikacji. Umożliwia użytkownikom tworzenie, uruchamianie i zarządzanie kontenerami, co pozwala na łatwe wdrażanie aplikacji w różnych środowiskach.

## Usage
Podstawowa składnia polecenia `docker` wygląda następująco:

```bash
docker [options] [arguments]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `docker`:

- `run`: uruchamia nowy kontener.
- `ps`: wyświetla uruchomione kontenery.
- `stop`: zatrzymuje działający kontener.
- `rm`: usuwa kontener.
- `images`: wyświetla listę obrazów dostępnych na lokalnej maszynie.

## Common Examples
Poniżej przedstawiono kilka praktycznych przykładów użycia polecenia `docker`:

1. **Uruchomienie nowego kontenera**:
   ```bash
   docker run hello-world
   ```

2. **Wyświetlenie uruchomionych kontenerów**:
   ```bash
   docker ps
   ```

3. **Zatrzymanie kontenera**:
   ```bash
   docker stop <container_id>
   ```

4. **Usunięcie kontenera**:
   ```bash
   docker rm <container_id>
   ```

5. **Wyświetlenie dostępnych obrazów**:
   ```bash
   docker images
   ```

## Tips
- Zawsze używaj opcji `-d` (detached mode), aby uruchomić kontener w tle, co pozwala na dalszą pracę w terminalu.
- Regularnie usuwaj nieużywane kontenery i obrazy, aby zaoszczędzić miejsce na dysku, używając polecenia `docker system prune`.
- Korzystaj z plików `Dockerfile` do automatyzacji procesu budowania obrazów, co ułatwia zarządzanie zależnościami aplikacji.