# [Linux] C Shell (csh) modprobe uso: Carica moduli del kernel

## Overview
Il comando `modprobe` è utilizzato per caricare e scaricare moduli del kernel in un sistema operativo Linux. Questo comando gestisce automaticamente le dipendenze tra i moduli, rendendo più semplice l'aggiunta o la rimozione di funzionalità dal kernel.

## Usage
La sintassi di base del comando `modprobe` è la seguente:

```csh
modprobe [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per `modprobe`:

- `-r` : Scarica un modulo dal kernel.
- `--list` : Mostra i moduli disponibili.
- `--show-depends` : Mostra le dipendenze del modulo specificato.
- `--quiet` : Riduce l'output del comando.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `modprobe`:

1. **Caricare un modulo**:
   ```csh
   modprobe nome_modulo
   ```

2. **Scaricare un modulo**:
   ```csh
   modprobe -r nome_modulo
   ```

3. **Mostrare le dipendenze di un modulo**:
   ```csh
   modprobe --show-depends nome_modulo
   ```

4. **Elencare i moduli disponibili**:
   ```csh
   modprobe --list
   ```

## Tips
- Assicurati di avere i permessi di root quando utilizzi `modprobe`, poiché è necessario per caricare e scaricare moduli del kernel.
- Controlla sempre le dipendenze di un modulo prima di tentare di caricarlo, per evitare errori.
- Utilizza l'opzione `--quiet` se desideri un output meno verboso, utile per script o automazioni.