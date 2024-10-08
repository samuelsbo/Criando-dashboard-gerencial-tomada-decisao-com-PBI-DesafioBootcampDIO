# Criando-dashboard-gerencial-tomada-decisao-com-PBI-DesafioBootcampDIO

# Relatório Gerencial de Vendas - Power BI

Este projeto contém um relatório gerencial das vendas de diferentes produtos ao redor do mundo, utilizando o Power BI para criar visualizações interativas e fornecer insights detalhados sobre unidades vendidas, receita, custos e lucros por segmento, país e produto.

## Sumário
- [Descrição do Projeto](#descrição-do-projeto)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Base de Dados](#base-de-dados)
- [Cálculos e Medidas](#cálculos-e-medidas)
- [Principais Insights](#principais-insights)
- [Conclusões](#conclusões)
- [Autor](#autor)

## Descrição do Projeto

Este relatório gerencial foi desenvolvido com o objetivo de fornecer uma visão clara e detalhada sobre as vendas e lucros de produtos em diferentes regiões e segmentos de mercado. Através do Power BI, criamos dashboards interativos que permitem aos usuários explorar os dados por diferentes filtros, como ano, país, produto e segmento. O relatório foi criado a partir de uma base de dados pré-processada em SQL e modelada no Power BI com um **Esquema Estrela**.

## Tecnologias Utilizadas
- **Power BI Desktop**: Para limpeza, preparação dos dados e criação dos dashboards.
- **SQL**: Para consultas e manipulação de dados.
- **Excel**: Para armazenamento de dados adicionais (se necessário).
  
## Base de Dados

A base de dados contém informações detalhadas sobre vendas e lucros, organizada em tabelas dimensionais e uma tabela fato, conforme a modelagem em **esquema estrela**. A tabela **financials_origem** está oculta, sendo a origem dos dados das demais tabelas, exceto a **DimData**, que foi criada no Power Query.

### Estrutura das Tabelas:

- **FactSales**: Contém os dados de vendas, custos (COGS), descontos, país, produto, segmento e datas.
- **DimProducts**: Informações sobre os produtos vendidos (nome do produto, valores de venda, etc.).
- **DimDiscount**: Informações sobre as faixas de desconto aplicadas.
- **DimCountry**: Detalhes sobre os países onde as vendas foram realizadas.
- **DimSegment**: Segmentos de mercado (Enterprise, Governo, Pequenas Empresas, etc.).
- **DimData**: Tabela temporal para análise de vendas por ano, trimestre, mês e dia.
- **Medidas**: Tabela com medidas DAX usadas para cálculos no relatório.

## Cálculos e Medidas

No Power BI, foram aplicadas diversas medidas calculadas com funções DAX para agregar e analisar os dados:

- **Total Sales**: `SUM(FactSales[Gross Sales])` — Soma total das vendas brutas.
- **Total Profit**: `SUM(FactSales[Profit])` — Soma total dos lucros.
- **Total COGS**: `SUM(FactSales[COGS])` — Soma do custo de mercadorias vendidas.
- **Total Discounts**: `SUM(FactSales[Discounts])` — Soma dos descontos concedidos.
- **Unidades Vendidas**: `SUM(FactSales[Units Sold])` — Quantidade total de unidades vendidas.

Essas medidas são usadas em gráficos de barras, colunas e linhas para fornecer uma análise detalhada do desempenho de vendas e lucros por diferentes filtros.

## Principais Insights

1. **Distribuição de Lucro por País**: O país com maior lucro foi a França, seguido de perto pela Alemanha e Canadá.
2. **Vendas ao Longo do Tempo**: O maior pico de vendas ocorreu em Dezembro de 2014, com um total de aproximadamente $12 milhões em vendas.
3. **Desempenho por Segmento**: O segmento Governamental gerou o maior lucro, seguido por Enterprise e Pequenas Empresas.
4. **Lucro por Produto**: O produto **Paseo** liderou em vendas e lucros, seguido pelos produtos **VTT** e **Velo**.

## Conclusões

O dashboard gerencial revela um excelente desempenho no segmento Governamental e nos produtos de alto valor agregado, como Paseo e VTT. Mesmo com custos elevados de fabricação, a empresa manteve margens de lucro positivas em suas operações globais. Este relatório permite a identificação de oportunidades de crescimento por produto e região, bem como o monitoramento de desempenho ao longo do tempo.

## Autor

Este projeto foi desenvolvido por Samuel Batista, baseado nas orientações da tutora Juliana Mascarenhas (@julianazanelatto). Sinta-se à vontade para entrar em contato ou contribuir com melhorias!
