# [Linux] Bash dig Uso: Consulta de DNS

O comando `dig` é utilizado para realizar consultas de DNS (Domain Name System), permitindo que os usuários obtenham informações sobre nomes de domínio e endereços IP.

## Overview
O `dig` é uma ferramenta de linha de comando que facilita a consulta a servidores DNS. Ele é amplamente utilizado para diagnosticar problemas de DNS, verificar registros de domínio e obter informações detalhadas sobre a resolução de nomes.

## Usage
A sintaxe básica do comando `dig` é a seguinte:

```bash
dig [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `dig`:

- `@servidor`: Especifica o servidor DNS a ser consultado.
- `-t tipo`: Define o tipo de registro DNS a ser consultado (por exemplo, A, AAAA, MX, etc.).
- `+short`: Exibe uma saída simplificada, mostrando apenas o resultado da consulta.
- `+trace`: Realiza uma consulta completa, mostrando o caminho de resolução do DNS.

## Common Examples

### Consultar um registro A
Para obter o endereço IP de um domínio:

```bash
dig example.com
```

### Consultar um registro MX
Para verificar os registros de troca de correio (Mail Exchange) de um domínio:

```bash
dig example.com -t MX
```

### Consultar um servidor DNS específico
Para consultar um servidor DNS específico, como o Google:

```bash
dig @8.8.8.8 example.com
```

### Saída simplificada
Para obter uma saída mais curta do resultado:

```bash
dig example.com +short
```

### Rastrear a resolução de DNS
Para ver o caminho completo da resolução de um nome de domínio:

```bash
dig example.com +trace
```

## Tips
- Use `+short` para obter resultados mais limpos e fáceis de ler, especialmente quando você só precisa do endereço IP.
- Sempre especifique um servidor DNS se estiver enfrentando problemas de resolução, pois isso pode ajudar a identificar onde está o problema.
- Combine `dig` com outras ferramentas como `grep` para filtrar resultados específicos ou `more` para paginar saídas longas.