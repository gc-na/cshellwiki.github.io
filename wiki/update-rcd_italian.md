# [Linux] Bash update-rc.d utilizzo: Gestire i servizi di avvio

## Overview
Il comando `update-rc.d` è utilizzato per gestire i servizi di avvio in sistemi basati su Debian. Permette di aggiungere, rimuovere o modificare i collegamenti simbolici nei runlevel, facilitando la configurazione dei servizi che devono essere avviati o arrestati automaticamente al boot del sistema.

## Usage
La sintassi di base del comando è la seguente:

```bash
update-rc.d [opzioni] [servizio] [comando]
```

## Common Options
Ecco alcune opzioni comuni per `update-rc.d`:

- `defaults`: Aggiunge i collegamenti simbolici per i runlevel predefiniti.
- `remove`: Rimuove i collegamenti simbolici per il servizio specificato.
- `enable`: Abilita il servizio per l'avvio automatico.
- `disable`: Disabilita il servizio dall'avvio automatico.

## Common Examples
Ecco alcuni esempi pratici dell'uso di `update-rc.d`:

1. **Aggiungere un servizio con impostazioni predefinite**:
   ```bash
   sudo update-rc.d nome_servizio defaults
   ```

2. **Rimuovere un servizio**:
   ```bash
   sudo update-rc.d nome_servizio remove
   ```

3. **Abilitare un servizio per l'avvio automatico**:
   ```bash
   sudo update-rc.d nome_servizio enable
   ```

4. **Disabilitare un servizio dall'avvio automatico**:
   ```bash
   sudo update-rc.d nome_servizio disable
   ```

## Tips
- Assicurati di avere i permessi di superutente (root) quando utilizzi `update-rc.d`, poiché le modifiche ai servizi di avvio richiedono privilegi elevati.
- Controlla sempre lo stato del servizio dopo aver apportato modifiche per assicurarti che funzioni come previsto.
- Utilizza `ls /etc/rc*.d/` per visualizzare i servizi attualmente configurati nei vari runlevel.