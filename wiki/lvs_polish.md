# [Linux] Bash lvs użycie: wyświetlanie informacji o logicznych woluminach

## Przegląd
Polecenie `lvs` jest używane w systemach Linux do wyświetlania informacji o logicznych woluminach zarządzanych przez system LVM (Logical Volume Manager). Umożliwia użytkownikom monitorowanie i zarządzanie przestrzenią dyskową w systemie.

## Użycie
Podstawowa składnia polecenia `lvs` jest następująca:

```bash
lvs [opcje] [argumenty]
```

## Częste opcje
- `-o` : Określa, które kolumny mają być wyświetlane.
- `-a` : Wyświetla wszystkie woluminy, w tym nieaktywne.
- `--units` : Umożliwia określenie jednostek wyświetlanych wartości (np. MB, GB).
- `-n` : Wyświetla tylko woluminy o podanej nazwie.

## Przykłady
1. Wyświetlenie wszystkich logicznych woluminów:
   ```bash
   lvs
   ```

2. Wyświetlenie szczegółowych informacji o woluminach z określonymi kolumnami:
   ```bash
   lvs -o +devices
   ```

3. Wyświetlenie wszystkich woluminów, w tym nieaktywnych:
   ```bash
   lvs -a
   ```

4. Wyświetlenie woluminów w jednostkach gigabajtów:
   ```bash
   lvs --units g
   ```

5. Wyświetlenie informacji tylko o woluminie o konkretnej nazwie:
   ```bash
   lvs -n nazwa_woluminu
   ```

## Wskazówki
- Używaj opcji `-o`, aby dostosować wyświetlane informacje do swoich potrzeb.
- Regularnie monitoruj swoje woluminy, aby uniknąć problemów z przestrzenią dyskową.
- Zawsze sprawdzaj dokumentację (`man lvs`), aby poznać wszystkie dostępne opcje i ich zastosowanie.