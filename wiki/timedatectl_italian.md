# [Linux] Bash timedatectl utilizzo: Gestire data e ora di sistema

## Overview
Il comando `timedatectl` è utilizzato per visualizzare e modificare le impostazioni di data e ora del sistema in ambienti Linux. Permette di gestire anche il fuso orario e la sincronizzazione dell'orologio di sistema.

## Usage
La sintassi di base del comando è la seguente:

```bash
timedatectl [opzioni] [argomenti]
```

## Common Options
- `status`: Mostra lo stato attuale della data e ora.
- `set-time`: Imposta manualmente la data e l'ora.
- `set-timezone`: Cambia il fuso orario del sistema.
- `set-ntp`: Abilita o disabilita la sincronizzazione automatica dell'orologio tramite NTP (Network Time Protocol).
- `list-timezones`: Elenca tutti i fusi orari disponibili.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `timedatectl`:

1. **Visualizzare lo stato attuale di data e ora:**
   ```bash
   timedatectl status
   ```

2. **Impostare manualmente la data e l'ora:**
   ```bash
   timedatectl set-time '2023-10-01 12:00:00'
   ```

3. **Cambiare il fuso orario:**
   ```bash
   timedatectl set-timezone Europe/Rome
   ```

4. **Abilitare la sincronizzazione NTP:**
   ```bash
   timedatectl set-ntp true
   ```

5. **Elencare tutti i fusi orari disponibili:**
   ```bash
   timedatectl list-timezones
   ```

## Tips
- Assicurati di avere i permessi di superutente (root) per modificare le impostazioni di data e ora.
- Controlla frequentemente lo stato della sincronizzazione NTP per garantire che il tuo sistema mantenga l'ora corretta.
- Utilizza `timedatectl list-timezones` per trovare il fuso orario corretto prima di impostarlo.