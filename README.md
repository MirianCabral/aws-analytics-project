# Análise de Dados com AWS (Em andamento)

Este projeto simula um pipeline de dados em ambiente cloud, utilizando os serviços da AWS para ingestão, tratamento análise e visualização de dados.

## Tecnologias e Serviços
- Amazon S3 - armazenamento de dados brutos
- Athena -  consultas SQL otimizadas
- AWS Glue Data Catalog - registro e gerenciamento de tabelas
- Amazon QuickSight - visualização de dados
- SQL - criação de queries para exploração de métricas

## Objetivo
Criar um fluxo completo de análise de dados para geração de insights estratégicos, utilizando ferramentas serveless da AWS e preparando os dados para visualização em dashboards.

## Estrutura do projeto
- 'dataset/': amostra dos dados utilizados
- 'sql/': consultas feitas no Athena
- 'dashboard/': imagens do painel no QuickSight

## Status
Projeto em desenvolvimento - atualmente na etapa de criação de tabelas e consultas no Athena.

## Como visualizar
Este projeto utiliza dados armazenados em buckets S3. As consultas podem ser executadas diretamente via Athena com os scripts em '/sql'. Os painéis do QuickSight porem ser visualizados na pasta '/dashboard', com prints dos resultados.

## Soluções técnicas
Durante a criação inicial das tabelas no Athena, houve um problema de leitura dos arquivos CSV: os nomes das colunas estavam sendo interpretados como parte dos dados, e não como cabeçalhos. Isso afetava diretamente a execução das queries SQL.
A solução foi recriar as tabelas no Athena com os parâmetros corretos de leitura, como o uso de 'skip.header.line.cout = 1', para garantir que o Athena identificasse corretamente os nomes das colunas.
