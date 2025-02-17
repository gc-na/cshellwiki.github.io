# [Linux] Bash ftp Uso: Transferência de arquivos via FTP

## Overview
O comando `ftp` (File Transfer Protocol) é utilizado para transferir arquivos entre um cliente e um servidor através do protocolo FTP. Ele permite que os usuários se conectem a servidores FTP, façam upload e download de arquivos, além de gerenciar diretórios.

## Usage
A sintaxe básica do comando `ftp` é a seguinte:

```bash
ftp [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `ftp`:

- `-i`: Desativa o modo interativo, permitindo transferências sem confirmação.
- `-n`: Impede que o ftp se conecte automaticamente ao servidor padrão.
- `-v`: Ativa o modo verboso, exibindo detalhes das operações realizadas.
- `-g`: Desativa a expansão de nomes de arquivos globais.

## Common Examples

### Conectar a um servidor FTP
Para se conectar a um servidor FTP, use o seguinte comando:

```bash
ftp ftp.exemplo.com
```

### Fazer login com um nome de usuário específico
Para se conectar e fazer login com um nome de usuário:

```bash
ftp -n ftp.exemplo.com
user nome_de_usuario
```

### Fazer upload de um arquivo
Para enviar um arquivo para o servidor FTP, utilize o comando `put`:

```bash
ftp> put arquivo.txt
```

### Fazer download de um arquivo
Para baixar um arquivo do servidor, use o comando `get`:

```bash
ftp> get arquivo.txt
```

### Listar arquivos no diretório remoto
Para visualizar os arquivos no diretório atual do servidor:

```bash
ftp> ls
```

## Tips
- Sempre use conexões seguras, como SFTP ou FTPS, quando possível, para proteger suas transferências de arquivos.
- Verifique as permissões de arquivo no servidor após transferências para garantir que os arquivos estejam acessíveis.
- Utilize o modo binário (`binary`) ao transferir arquivos não-textuais, como imagens ou executáveis, para evitar corrupção de dados.