# [Linux] Bash udevadm Uso: Gerenciar dispositivos no sistema

## Overview
O comando `udevadm` é uma ferramenta utilizada para interagir com o sistema de gerenciamento de dispositivos do Linux, conhecido como udev. Ele permite que os usuários monitorem e gerenciem eventos de dispositivos, além de fornecer informações sobre os dispositivos conectados ao sistema.

## Usage
A sintaxe básica do comando `udevadm` é a seguinte:

```bash
udevadm [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `udevadm`:

- `info`: Exibe informações sobre um dispositivo específico.
- `trigger`: Aciona eventos de dispositivos, como a adição ou remoção de dispositivos.
- `settle`: Espera até que todos os eventos de dispositivos tenham sido processados.
- `control`: Permite iniciar ou parar o daemon udev.

## Common Examples
Aqui estão alguns exemplos práticos de uso do `udevadm`:

1. **Exibir informações sobre um dispositivo específico**:
   ```bash
   udevadm info --query=all --name=/dev/sda
   ```

2. **Acionar eventos para todos os dispositivos**:
   ```bash
   udevadm trigger
   ```

3. **Esperar até que todos os eventos de dispositivos sejam processados**:
   ```bash
   udevadm settle
   ```

4. **Controlar o daemon udev**:
   ```bash
   udevadm control --reload-rules
   ```

## Tips
- Sempre verifique as permissões necessárias ao usar `udevadm`, pois algumas operações podem exigir privilégios de superusuário.
- Use `udevadm monitor` para acompanhar eventos em tempo real, o que pode ser útil para depuração.
- Familiarize-se com as regras do udev, pois elas determinam como os dispositivos são gerenciados e reconhecidos pelo sistema.