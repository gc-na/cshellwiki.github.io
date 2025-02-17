# [Linux] Bash tune2fs uso: Ajustar parâmetros de sistemas de arquivos ext2/ext3/ext4

## Overview
O comando `tune2fs` é utilizado para ajustar parâmetros de sistemas de arquivos do tipo ext2, ext3 e ext4. Ele permite modificar características do sistema de arquivos, como a quantidade de inodes, a frequência de verificação e outras opções que podem otimizar o desempenho e a integridade do sistema.

## Usage
A sintaxe básica do comando `tune2fs` é a seguinte:

```bash
tune2fs [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `tune2fs`:

- `-c <n>`: Define o número máximo de montagens antes de uma verificação do sistema de arquivos.
- `-i <intervalo>`: Define o intervalo de tempo entre verificações do sistema de arquivos.
- `-m <porcentagem>`: Define a porcentagem do sistema de arquivos reservada para o usuário root.
- `-O <opções>`: Ativa as opções especificadas para o sistema de arquivos.
- `-L <rótulo>`: Define um novo rótulo para o sistema de arquivos.
- `-E <opções estendidas>`: Define opções estendidas para o sistema de arquivos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `tune2fs`:

1. **Definir o número máximo de montagens antes da verificação:**
   ```bash
   tune2fs -c 20 /dev/sda1
   ```

2. **Definir o intervalo de tempo entre verificações para 30 dias:**
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

3. **Reservar 5% do sistema de arquivos para o usuário root:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. **Ativar a opção de journaling:**
   ```bash
   tune2fs -O has_journal /dev/sda1
   ```

5. **Definir um novo rótulo para o sistema de arquivos:**
   ```bash
   tune2fs -L "MeuSistema" /dev/sda1
   ```

## Tips
- Sempre faça um backup dos dados antes de usar o `tune2fs`, pois algumas operações podem afetar a integridade do sistema de arquivos.
- Utilize o comando `tune2fs -l /dev/sda1` para listar as opções atuais do sistema de arquivos antes de fazer alterações.
- Evite realizar alterações em sistemas de arquivos montados, a menos que seja absolutamente necessário, para evitar corrupção de dados.