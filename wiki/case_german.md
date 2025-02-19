# [Linux] C Shell (csh) case Verwendung: Mustervergleich und bedingte Ausführung

## Übersicht
Der Befehl `case` in der C Shell (csh) wird verwendet, um Mustervergleiche durchzuführen und verschiedene Befehle basierend auf dem Ergebnis des Vergleichs auszuführen. Dies ist besonders nützlich, um Entscheidungen in Skripten zu treffen.

## Verwendung
Die grundlegende Syntax des `case`-Befehls sieht wie folgt aus:

```csh
case [variable] in
    [muster1]) [befehl1];;
    [muster2]) [befehl2];;
    ...
    *) [standardbefehl];;
esac
```

## Häufige Optionen
- `*)`: Dies ist das Standardmuster, das ausgeführt wird, wenn keines der vorherigen Muster übereinstimmt.

## Häufige Beispiele

### Beispiel 1: Einfache Musterübereinstimmung
```csh
set var = "apple"
case $var in
    apple) echo "Das ist ein Apfel";;
    banana) echo "Das ist eine Banane";;
    *) echo "Unbekannte Frucht";;
esac
```

### Beispiel 2: Verwendung von Platzhaltern
```csh
set datei = "bericht.txt"
case $datei in
    *.txt) echo "Dies ist eine Textdatei";;
    *.jpg) echo "Dies ist ein Bild";;
    *) echo "Unbekannte Dateityp";;
esac
```

### Beispiel 3: Mehrere Muster
```csh
set tier = "Hund"
case $tier in
    Hund|Katze) echo "Das ist ein Haustier";;
    Vogel) echo "Das ist ein Vogel";;
    *) echo "Unbekanntes Tier";;
esac
```

## Tipps
- Verwenden Sie Platzhalter wie `*` und `?`, um flexiblere Mustervergleiche zu ermöglichen.
- Achten Sie darauf, dass die Muster in der Reihenfolge von spezifisch zu allgemein angeordnet sind, um die gewünschte Übereinstimmung zu gewährleisten.
- Nutzen Sie das Standardmuster `*)`, um sicherzustellen, dass immer ein Befehl ausgeführt wird, auch wenn keine der vorherigen Bedingungen erfüllt ist.