# [Linux] Bash flatpak użycie: zarządzanie aplikacjami w kontenerach

## Overview
Polecenie `flatpak` służy do zarządzania aplikacjami w kontenerach, co pozwala na instalację, aktualizację i uruchamianie aplikacji w izolowanym środowisku. Dzięki temu aplikacje mogą działać niezależnie od systemu operacyjnego i jego bibliotek.

## Usage
Podstawowa składnia polecenia `flatpak` jest następująca:

```bash
flatpak [opcje] [argumenty]
```

## Common Options
- `install`: Instaluje aplikację z repozytoriów Flatpak.
- `uninstall`: Usuwa zainstalowaną aplikację.
- `update`: Aktualizuje zainstalowane aplikacje do najnowszych wersji.
- `list`: Wyświetla listę zainstalowanych aplikacji.
- `run`: Uruchamia zainstalowaną aplikację.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `flatpak`:

### Instalacja aplikacji
Aby zainstalować aplikację, użyj polecenia:

```bash
flatpak install flathub org.videolan.VLC
```

### Usuwanie aplikacji
Aby usunąć zainstalowaną aplikację, wykonaj:

```bash
flatpak uninstall org.videolan.VLC
```

### Aktualizacja aplikacji
Aby zaktualizować wszystkie zainstalowane aplikacje, użyj:

```bash
flatpak update
```

### Wyświetlanie zainstalowanych aplikacji
Aby zobaczyć listę zainstalowanych aplikacji, wpisz:

```bash
flatpak list
```

### Uruchamianie aplikacji
Aby uruchomić zainstalowaną aplikację, użyj:

```bash
flatpak run org.videolan.VLC
```

## Tips
- Zawsze sprawdzaj dostępność aktualizacji, aby korzystać z najnowszych funkcji i poprawek bezpieczeństwa.
- Używaj repozytoriów Flathub, aby mieć dostęp do szerokiej gamy aplikacji.
- Pamiętaj, że aplikacje uruchamiane przez Flatpak mogą mieć ograniczony dostęp do zasobów systemowych, co zwiększa bezpieczeństwo.