# [Linux] C Shell (csh) paste Uso equivalente: Unire file riga per riga

## Overview
Il comando `paste` in C Shell (csh) è utilizzato per unire file di testo riga per riga. Questo comando permette di combinare il contenuto di più file in un'unica uscita, separando le righe con un delimitatore specificato.

## Usage
La sintassi di base del comando `paste` è la seguente:

```csh
paste [options] [arguments]
```

## Common Options
- `-d DELIMITER`: Specifica un delimitatore personalizzato per separare le righe unite. Se non specificato, il delimitatore predefinito è una tabulazione.
- `-s`: Unisce le righe di ciascun file in una sola riga, invece di unire file diversi riga per riga.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `paste`:

1. **Unire due file con il delimitatore predefinito (tabulazione)**:
   ```csh
   paste file1.txt file2.txt
   ```

2. **Unire due file utilizzando un delimitatore personalizzato (ad esempio, una virgola)**:
   ```csh
   paste -d ',' file1.txt file2.txt
   ```

3. **Unire le righe di un singolo file in una sola riga**:
   ```csh
   paste -s file1.txt
   ```

4. **Unire più file e specificare un delimitatore**:
   ```csh
   paste -d '|' file1.txt file2.txt file3.txt
   ```

## Tips
- Quando si utilizza il delimitatore personalizzato, assicurati che il carattere scelto non sia presente nel contenuto dei file per evitare confusione.
- Puoi combinare `paste` con altri comandi come `sort` o `uniq` per ottenere risultati più complessi.
- Ricorda che `paste` non modifica i file originali; produce solo un'uscita combinata. Se desideri salvare l'uscita in un nuovo file, puoi reindirizzare l'output:
  ```csh
  paste file1.txt file2.txt > output.txt
  ```