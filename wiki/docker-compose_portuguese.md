# [Linux] Bash docker-compose uso: Gerenciar aplicações em contêineres

## Overview
O comando `docker-compose` é uma ferramenta que permite definir e executar aplicações Docker multi-contêiner. Com ele, você pode configurar serviços, redes e volumes em um único arquivo YAML, facilitando o gerenciamento de ambientes complexos.

## Usage
A sintaxe básica do comando `docker-compose` é a seguinte:

```bash
docker-compose [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `docker-compose`:

- `up`: Inicia os contêineres definidos no arquivo `docker-compose.yml`.
- `down`: Para e remove os contêineres, redes e volumes criados pelo comando `up`.
- `build`: Constrói ou reconstrói os serviços definidos.
- `logs`: Exibe os logs dos contêineres em execução.
- `ps`: Lista os contêineres em execução e seus estados.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `docker-compose`:

1. **Iniciar os serviços definidos**:
   ```bash
   docker-compose up
   ```

2. **Iniciar os serviços em segundo plano**:
   ```bash
   docker-compose up -d
   ```

3. **Parar e remover os serviços**:
   ```bash
   docker-compose down
   ```

4. **Construir os serviços antes de iniciar**:
   ```bash
   docker-compose up --build
   ```

5. **Exibir logs dos serviços**:
   ```bash
   docker-compose logs
   ```

6. **Listar os contêineres em execução**:
   ```bash
   docker-compose ps
   ```

## Tips
- Sempre use o arquivo `docker-compose.yml` para definir claramente os serviços e suas dependências.
- Utilize a opção `-d` para executar os contêineres em segundo plano, especialmente em ambientes de produção.
- Mantenha seu arquivo `docker-compose.yml` bem documentado para facilitar a manutenção e o entendimento por outros desenvolvedores.
- Use `docker-compose down --volumes` se precisar remover também os volumes associados aos contêineres.