# [Linux] Bash sftp Uso: Transferir arquivos de forma segura

## Overview
O comando `sftp` (Secure File Transfer Protocol) é utilizado para transferir arquivos de forma segura entre um cliente e um servidor. Ele utiliza o protocolo SSH (Secure Shell) para garantir que os dados sejam criptografados durante a transmissão, oferecendo uma alternativa segura ao tradicional FTP.

## Usage
A sintaxe básica do comando `sftp` é a seguinte:

```bash
sftp [opções] [usuário@host]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `sftp`:

- `-b arquivo`: Executa comandos de um arquivo em vez de interagir diretamente.
- `-C`: Ativa a compressão durante a transferência de dados.
- `-i arquivo`: Especifica um arquivo de chave privada para autenticação.
- `-P porta`: Especifica a porta a ser usada para a conexão.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o comando `sftp`:

1. **Conectar a um servidor SFTP:**
   ```bash
   sftp usuario@exemplo.com
   ```

2. **Transferir um arquivo do cliente para o servidor:**
   ```bash
   sftp usuario@exemplo.com
   put arquivo.txt
   ```

3. **Transferir um arquivo do servidor para o cliente:**
   ```bash
   sftp usuario@exemplo.com
   get arquivo.txt
   ```

4. **Listar arquivos no diretório remoto:**
   ```bash
   sftp usuario@exemplo.com
   ls
   ```

5. **Usar um arquivo de comandos:**
   ```bash
   sftp -b comandos.txt usuario@exemplo.com
   ```

## Tips
- Sempre use `sftp` em vez de `ftp` para garantir que suas transferências de arquivos sejam seguras.
- Considere usar a opção `-C` para acelerar a transferência de arquivos grandes, especialmente em conexões lentas.
- Mantenha suas chaves SSH seguras e utilize autenticação baseada em chave sempre que possível para aumentar a segurança.