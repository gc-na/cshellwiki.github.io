# [Linux] Bash netstat Uso: Exibe conexões de rede e estatísticas

## Overview
O comando `netstat` é uma ferramenta de linha de comando que exibe informações sobre conexões de rede, tabelas de roteamento, interfaces de rede e estatísticas de protocolo. Ele é útil para diagnosticar problemas de rede e monitorar o tráfego.

## Usage
A sintaxe básica do comando `netstat` é a seguinte:

```bash
netstat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `netstat`:

- `-a`: Exibe todas as conexões e escuta as portas.
- `-t`: Mostra apenas conexões TCP.
- `-u`: Mostra apenas conexões UDP.
- `-n`: Exibe endereços e números de porta em formato numérico.
- `-l`: Exibe apenas as portas que estão escutando.
- `-p`: Mostra o PID e o nome do programa que está utilizando a conexão.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `netstat`:

1. **Exibir todas as conexões e portas em escuta:**
   ```bash
   netstat -a
   ```

2. **Mostrar apenas conexões TCP:**
   ```bash
   netstat -t
   ```

3. **Mostrar conexões UDP em formato numérico:**
   ```bash
   netstat -u -n
   ```

4. **Exibir portas que estão escutando:**
   ```bash
   netstat -l
   ```

5. **Verificar quais programas estão usando as conexões:**
   ```bash
   netstat -p
   ```

## Tips
- Utilize a opção `-n` para acelerar a exibição de resultados, evitando a resolução de nomes de host.
- Combine opções para obter informações mais detalhadas, como `netstat -tulnp` para ver conexões TCP e UDP em escuta com detalhes do programa.
- Considere usar `netstat` em conjunto com outros comandos, como `grep`, para filtrar resultados específicos. Por exemplo:
  ```bash
  netstat -tuln | grep LISTEN
  ```