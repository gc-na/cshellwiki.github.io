# [Linux] Bash mysql uso: Interagir com bancos de dados MySQL

## Overview
O comando `mysql` é uma ferramenta de linha de comando que permite interagir com bancos de dados MySQL. Ele é utilizado para executar consultas SQL, gerenciar bancos de dados e realizar operações administrativas.

## Usage
A sintaxe básica do comando `mysql` é a seguinte:

```bash
mysql [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `mysql`:

- `-u`: Especifica o nome de usuário para se conectar ao banco de dados.
- `-p`: Solicita a senha do usuário.
- `-h`: Define o host do servidor MySQL (por padrão, é `localhost`).
- `-D`: Especifica o banco de dados a ser utilizado.
- `--execute`: Permite executar uma consulta SQL diretamente da linha de comando.

## Common Examples

### Conectar ao MySQL
Para se conectar ao MySQL como um usuário específico:

```bash
mysql -u usuario -p
```

### Executar uma consulta SQL
Para executar uma consulta SQL diretamente:

```bash
mysql -u usuario -p -e "SELECT * FROM nome_da_tabela;"
```

### Conectar a um banco de dados específico
Para se conectar a um banco de dados específico ao iniciar o cliente MySQL:

```bash
mysql -u usuario -p -D nome_do_banco
```

### Importar um arquivo SQL
Para importar um arquivo SQL para um banco de dados:

```bash
mysql -u usuario -p nome_do_banco < arquivo.sql
```

### Exportar um banco de dados
Para exportar um banco de dados para um arquivo SQL:

```bash
mysqldump -u usuario -p nome_do_banco > arquivo.sql
```

## Tips
- Sempre use a opção `-p` para garantir que sua senha não seja exposta na linha de comando.
- Utilize o comando `SHOW DATABASES;` após conectar-se ao MySQL para visualizar os bancos de dados disponíveis.
- Para sair do cliente MySQL, basta digitar `exit;` ou `quit;`.
- Considere usar scripts SQL para automatizar tarefas comuns e facilitar a manutenção do banco de dados.