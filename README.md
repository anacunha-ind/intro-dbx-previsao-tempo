# Hands-on: Pipeline ELT com Delta Lake
**Programa LH — Módulo 2: Introdução ao Databricks**

---

## Sobre

Notebook hands-on para construção de um pipeline ELT completo no Databricks, usando dados reais da [API Open-Meteo](https://open-meteo.com/) (previsão do tempo — São Paulo).

## Estrutura

```
aularaw.<seu_nome>.previsao           ← Bronze: dado bruto da API
aulaproducao.<seu_nome>.previsao_silver  ← Silver: dado transformado
aulaproducao.<seu_nome>.previsao_gold    ← Gold: agregação diária
```

## Pré-requisitos

- Acesso ao workspace Databricks da aula
- Cluster All-Purpose ou Serverless conectado
- Schemas criados pelo instrutor: `aularaw.<seu_nome>` e `aulaproducao.<seu_nome>`

## Como usar

1. Importar o notebook: **Workspace → Import → selecionar o `.ipynb`**
2. Na célula de setup, substituir `SEU_NOME` pelo seu nome (sem espaços ou acentos)
3. Executar as células em ordem

## Conteúdo

| Passo | Descrição |
|-------|-----------|
| Setup | Variáveis e criação de schemas |
| 1 | Magic commands e `dbutils` |
| 2 | Leitura da API Open-Meteo (Bronze) |
| 3 | Conversão Pandas → Spark |
| 4 | Salvar Bronze como Delta Table |
| 5 | Transformações Bronze → Silver |
| 6 | Queries SQL na Silver |
| 7 | `DESCRIBE HISTORY` e Time Travel |
| 8 | Agregação e camada Gold |
| 9 | Exploração no Data Explorer (Unity Catalog) |

## Adaptação para Free Edition

O notebook inclui uma seção ao final com a versão adaptada para o **Databricks Community Edition**, usando databases Hive no lugar de catálogos Unity Catalog.
