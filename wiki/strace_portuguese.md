# [Linux] Bash strace uso: rastrear chamadas de sistema

## Overview
O comando `strace` é uma ferramenta poderosa utilizada para rastrear chamadas de sistema e sinais recebidos por um processo em execução no Linux. Ele permite que os desenvolvedores e administradores de sistema entendam melhor o comportamento de programas, diagnosticando problemas e analisando a interação entre o software e o sistema operacional.

## Usage
A sintaxe básica do comando `strace` é a seguinte:

```bash
strace [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `strace`:

- `-c`: Resumo das estatísticas de chamadas de sistema.
- `-e`: Filtra as chamadas de sistema a serem rastreadas (por exemplo, `-e trace=open`).
- `-o <arquivo>`: Redireciona a saída para um arquivo em vez de exibi-la no terminal.
- `-p <PID>`: Anexa ao processo com o ID especificado (PID).
- `-f`: Segue processos filhos criados por fork.

## Common Examples

### Rastrear um comando simples
Para rastrear um comando simples, como `ls`, você pode usar:

```bash
strace ls
```

### Rastrear chamadas de sistema específicas
Se você deseja rastrear apenas chamadas de sistema relacionadas a arquivos, use:

```bash
strace -e trace=open,close ls
```

### Redirecionar a saída para um arquivo
Para salvar a saída do `strace` em um arquivo, utilize:

```bash
strace -o rastreamento.txt ls
```

### Anexar a um processo em execução
Para anexar o `strace` a um processo já em execução, primeiro descubra o PID do processo e, em seguida, use:

```bash
strace -p <PID>
```

### Resumo das estatísticas de chamadas
Para obter um resumo das chamadas de sistema feitas por um comando, você pode usar:

```bash
strace -c ls
```

## Tips
- Use a opção `-o` para salvar a saída em um arquivo, facilitando a análise posterior.
- Combine `-e` com opções de filtragem para focar em chamadas de sistema específicas, tornando a saída mais gerenciável.
- Lembre-se de que o `strace` pode afetar o desempenho do programa rastreado, especialmente em aplicativos que fazem muitas chamadas de sistema.
- Utilize `strace` em ambientes de teste sempre que possível, para evitar impactos em sistemas de produção.