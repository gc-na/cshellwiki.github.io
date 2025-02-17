# [Linux] Bash swapon Uso: Ativar espaço de troca

## Overview
O comando `swapon` é utilizado para ativar dispositivos ou arquivos de swap no sistema Linux. O swap é uma área no disco rígido que o sistema utiliza como memória virtual, permitindo que ele gerencie a memória de forma mais eficiente, especialmente quando a RAM está cheia.

## Usage
A sintaxe básica do comando `swapon` é a seguinte:

```bash
swapon [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `swapon`:

- `-a`: Ativa todas as áreas de swap listadas no arquivo `/etc/fstab`.
- `-e`: Ignora erros ao ativar áreas de swap.
- `--show`: Exibe informações sobre as áreas de swap ativas.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `swapon`:

1. **Ativar uma área de swap específica**:
   ```bash
   swapon /dev/sdX
   ```
   Substitua `/dev/sdX` pelo caminho do dispositivo de swap que você deseja ativar.

2. **Ativar todas as áreas de swap listadas no fstab**:
   ```bash
   swapon -a
   ```

3. **Mostrar as áreas de swap ativas**:
   ```bash
   swapon --show
   ```

4. **Ativar um arquivo de swap**:
   Primeiro, crie um arquivo de swap:
   ```bash
   fallocate -l 1G /swapfile
   chmod 600 /swapfile
   mkswap /swapfile
   ```
   Em seguida, ative o arquivo de swap:
   ```bash
   swapon /swapfile
   ```

## Tips
- Sempre verifique se a área de swap foi ativada corretamente usando `swapon --show` após executar o comando.
- Para garantir que a área de swap seja ativada automaticamente na inicialização, adicione a entrada correspondente no arquivo `/etc/fstab`.
- Use o comando `free -h` para monitorar o uso da memória e do swap em tempo real.