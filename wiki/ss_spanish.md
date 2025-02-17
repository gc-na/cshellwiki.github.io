# [Linux] Bash ss uso equivalente: [visualizar conexiones de red]

## Overview
El comando `ss` se utiliza en sistemas Linux para investigar y mostrar información sobre conexiones de red. Es una herramienta poderosa que permite a los administradores de sistemas y a los usuarios obtener detalles sobre los sockets de red, tanto en estado de escucha como en conexión.

## Usage
La sintaxis básica del comando `ss` es la siguiente:

```bash
ss [opciones] [argumentos]
```

## Common Options
Aquí hay algunas opciones comunes que puedes usar con `ss`:

- `-t`: Muestra solo conexiones TCP.
- `-u`: Muestra solo conexiones UDP.
- `-l`: Muestra solo sockets en estado de escucha.
- `-p`: Muestra el proceso que está utilizando el socket.
- `-n`: Muestra direcciones y puertos en formato numérico, evitando la resolución de nombres.

## Common Examples
A continuación, se presentan algunos ejemplos prácticos del uso del comando `ss`:

1. **Mostrar todas las conexiones TCP:**
   ```bash
   ss -t
   ```

2. **Mostrar todas las conexiones UDP:**
   ```bash
   ss -u
   ```

3. **Mostrar sockets en estado de escucha:**
   ```bash
   ss -l
   ```

4. **Mostrar conexiones con información del proceso:**
   ```bash
   ss -p
   ```

5. **Mostrar todas las conexiones con detalles numéricos:**
   ```bash
   ss -n
   ```

## Tips
- Usa `ss -tuln` para ver todas las conexiones TCP y UDP en estado de escucha con detalles numéricos.
- Combina opciones para obtener información más específica, como `ss -tunlp` para ver conexiones TCP y UDP junto con el proceso correspondiente.
- Recuerda que `ss` es más rápido y consume menos recursos que el comando `netstat`, por lo que es preferido en sistemas modernos.