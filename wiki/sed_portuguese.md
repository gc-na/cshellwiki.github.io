# [Linux] Bash sed Uso equivalente: Editar texto em fluxo

## Overview
O comando `sed` (stream editor) é uma ferramenta poderosa utilizada para manipular e transformar texto em fluxo. Ele permite realizar operações como substituição, inserção e exclusão de texto em arquivos ou na saída de outros comandos.

## Usage
A sintaxe básica do comando `sed` é a seguinte:

```bash
sed [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `sed`:

- `-e`: Permite adicionar múltiplas expressões de edição.
- `-i`: Edita os arquivos no local, ou seja, faz as alterações diretamente no arquivo.
- `-n`: Suprime a saída padrão, permitindo que você controle o que é exibido com o comando `p` (print).
- `s/padrão/substituição/`: Realiza uma substituição de um padrão por um texto específico.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `sed`:

### 1. Substituir texto em um arquivo
Substitui todas as ocorrências da palavra "antigo" por "novo" em um arquivo chamado `exemplo.txt`.

```bash
sed -i 's/antigo/novo/g' exemplo.txt
```

### 2. Exibir linhas que contêm um padrão
Exibe apenas as linhas que contêm a palavra "importante" em um arquivo.

```bash
sed -n '/importante/p' exemplo.txt
```

### 3. Remover linhas vazias
Remove todas as linhas vazias de um arquivo.

```bash
sed -i '/^$/d' exemplo.txt
```

### 4. Adicionar texto antes de uma linha específica
Adiciona a linha "Nota: " antes de cada linha que contém "aviso".

```bash
sed -i '/aviso/i Nota: ' exemplo.txt
```

### 5. Alterar a primeira ocorrência de um padrão
Altera apenas a primeira ocorrência da palavra "erro" para "correção".

```bash
sed -i '0,/erro/s//correção/' exemplo.txt
```

## Tips
- Sempre faça um backup dos seus arquivos antes de usar a opção `-i`, pois as alterações são irreversíveis.
- Utilize `sed` em combinação com outros comandos, como `grep` e `awk`, para manipulações mais complexas.
- Teste suas expressões `sed` em um terminal antes de aplicá-las em arquivos importantes para garantir que funcionem como esperado.