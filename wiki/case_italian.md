# [Linux] C Shell (csh) case: Gestione delle condizioni

## Overview
Il comando `case` nel C Shell (csh) è utilizzato per eseguire confronti di pattern su variabili. Permette di eseguire diverse azioni in base al valore di una variabile, rendendo il controllo del flusso nei script molto più semplice e leggibile.

## Usage
La sintassi di base del comando `case` è la seguente:

```csh
case [variabile] in
    [pattern1]) [comando1];;
    [pattern2]) [comando2];;
    ...
    *) [comando_default];;
esac
```

## Common Options
Il comando `case` non ha opzioni specifiche, ma i pattern possono includere:
- `*` - corrisponde a qualsiasi stringa.
- `?` - corrisponde a un singolo carattere.
- `[abc]` - corrisponde a uno dei caratteri specificati.

## Common Examples

### Esempio 1: Controllo del giorno della settimana
```csh
set giorno = `date +%A`
case $giorno in
    Lunedì) echo "Inizio settimana!";;
    Venerdì) echo "Quasi weekend!";;
    Sabato|Domenica) echo "Buon fine settimana!";;
    *) echo "Un giorno normale."; 
esac
```

### Esempio 2: Gestione delle estensioni dei file
```csh
set file = "documento.txt"
case $file in
    *.txt) echo "Questo è un file di testo.";;
    *.jpg|*.png) echo "Questo è un'immagine.";;
    *) echo "Tipo di file sconosciuto.";;
esac
```

### Esempio 3: Opzioni dell'utente
```csh
set scelta = $1
case $scelta in
    -h|--help) echo "Mostra aiuto";;
    -v|--version) echo "Versione 1.0";;
    *) echo "Opzione non valida";;
esac
```

## Tips
- Utilizza i pattern in modo strategico per semplificare il codice e migliorare la leggibilità.
- Ricorda di utilizzare `;;` alla fine di ogni blocco di comandi per terminare il caso.
- Fai attenzione all'ordine dei pattern, poiché il primo corrispondente verrà eseguito.