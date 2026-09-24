# mvp-engenharia-dados-prf
MVP de Engenharia de Dados — Pipeline em Databricks para análise de acidentes em rodovias federais brasileiras (PRF, 2017–2025).

# MVP Engenharia de Dados — Acidentes em Rodovias Federais

Projeto desenvolvido como MVP da disciplina de Engenharia de Dados.

## Objetivo

Construir um pipeline de dados em nuvem para coletar, organizar, tratar, integrar e analisar dados públicos de acidentes em rodovias federais brasileiras, buscando identificar tendências históricas, padrões sazonais, diferenças regionais e fatores associados à ocorrência e à fatalidade dos acidentes.

## Fontes de dados

- Polícia Rodoviária Federal (PRF) — Dados Abertos de acidentes em rodovias federais, período de 2017 a 2025.
- ANBIMA — Calendário de feriados nacionais.

## Plataforma

O pipeline foi desenvolvido no Databricks Free Edition utilizando Apache Spark e tabelas Delta.

## Arquitetura

O projeto utiliza uma arquitetura em três camadas:

- **Bronze:** armazenamento dos arquivos originais.
- **Silver:** consolidação, limpeza e integração dos dados.
- **Gold:** enriquecimento e preparação dos dados para análise.

Fluxo:

PRF + ANBIMA → Bronze → Silver → Gold → Análises

## Principais etapas

1. Coleta dos arquivos públicos.
2. Armazenamento dos dados originais em Databricks Volume.
3. Consolidação dos arquivos anuais da PRF.
4. Tratamento e padronização dos dados.
5. Integração com o calendário de feriados.
6. Criação da camada analítica Gold.
7. Avaliação da qualidade dos dados.
8. Análise das questões definidas no estudo.

## Tecnologias utilizadas

- Databricks
- Apache Spark / PySpark
- Delta Lake
- Python
- Pandas

## Estrutura do repositório

`notebooks/` — notebook contendo o pipeline, documentação e análises do projeto.

### Visualizações

O notebook foi desenvolvido e executado originalmente no Databricks. Algumas visualizações foram produzidas utilizando os recursos gráficos nativos da plataforma e, por esse motivo, podem não ser renderizadas pelo visualizador de notebooks do GitHub. Os dados utilizados nessas visualizações e os respectivos resultados tabulares permanecem disponíveis no notebook.

## Autor

Diogo Bobsin
