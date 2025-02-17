# [Linux] Bash hostname uso: Exibir e definir o nome do host

## Overview
O comando `hostname` é utilizado para exibir ou definir o nome do host do sistema. O nome do host é um identificador que permite que o sistema seja reconhecido em uma rede. 

## Usage
A sintaxe básica do comando é a seguinte:

```
hostname [opções] [argumentos]
```

## Common Options
- `-a`, `--alias`: Exibe o nome do host alternativo.
- `-d`, `--domain`: Mostra o nome do domínio do host.
- `-f`, `--fqdn`: Exibe o nome de domínio totalmente qualificado (FQDN).
- `-i`, `--ip-address`: Mostra o endereço IP do host.
- `-s`, `--short`: Exibe apenas o nome do host sem o domínio.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `hostname`:

1. **Exibir o nome do host atual:**
   ```bash
   hostname
   ```

2. **Exibir o nome de domínio totalmente qualificado:**
   ```bash
   hostname -f
   ```

3. **Exibir o endereço IP do host:**
   ```bash
   hostname -i
   ```

4. **Definir um novo nome de host:**
   ```bash
   sudo hostname novo-nome
   ```

5. **Exibir o nome do domínio:**
   ```bash
   hostname -d
   ```

## Tips
- Sempre use `sudo` ao definir um novo nome de host para garantir que você tenha as permissões necessárias.
- Após alterar o nome do host, pode ser necessário reiniciar o sistema ou reiniciar serviços de rede para que as mudanças tenham efeito.
- Para verificar se a mudança foi bem-sucedida, use o comando `hostname` novamente após a alteração.