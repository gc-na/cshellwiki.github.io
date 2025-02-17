# [Linux] Bash env Uso: [executar comandos com variáveis de ambiente]

## Overview
O comando `env` é utilizado para executar um comando em um ambiente modificado. Ele permite que você defina variáveis de ambiente temporárias e execute um programa com essas variáveis, sem alterar o ambiente global do sistema.

## Usage
A sintaxe básica do comando `env` é a seguinte:

```bash
env [opções] [argumentos]
```

## Common Options
- `-i`: Ignora o ambiente atual e inicia um novo ambiente vazio.
- `-u VAR`: Remove a variável de ambiente especificada antes de executar o comando.
- `VAR=value`: Define uma variável de ambiente temporária para o comando que será executado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `env`:

1. **Executar um comando com uma variável de ambiente temporária:**

```bash
env VAR1=valor1 comando
```

2. **Ignorar o ambiente atual e executar um comando:**

```bash
env -i comando
```

3. **Remover uma variável de ambiente antes de executar um comando:**

```bash
env -u VAR1 comando
```

4. **Definir várias variáveis de ambiente:**

```bash
env VAR1=valor1 VAR2=valor2 comando
```

## Tips
- Use `env` para testar como um comando se comporta em um ambiente limpo, sem interferência de variáveis de ambiente existentes.
- Quando precisar executar um script com variáveis de ambiente específicas, `env` pode ser uma maneira eficaz de evitar conflitos.
- Para verificar as variáveis de ambiente atuais, você pode usar `env` sem argumentos.