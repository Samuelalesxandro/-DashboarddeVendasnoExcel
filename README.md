# Dashboard de Vendas no Excel

## 📌 Objetivo
Este projeto tem como objetivo transformar dados brutos de vendas em um **dashboard interativo no Excel**, com indicadores e visualizações que apoiam a análise de desempenho e a tomada de decisão baseada em dados.

## 📊 O que o dashboard entrega
O dashboard permite analisar as vendas por diferentes perspectivas, como período, região, produto e vendedor (dependendo do dataset), incluindo:

- **KPIs principais**:
  - Receita Total
  - Quantidade Vendida
  - Nº de Pedidos
  - Ticket Médio
  - (Opcional) Lucro e Margem

- **Visualizações**:
  - Receita ao longo do tempo (linha)
  - Top produtos / categorias (barras)
  - Participação por canal/região (pizza/treemap/barras)
  - (Opcional) Heatmap por dia/semana ou calendário

- **Filtros (Slicers)**:
  - Ano/Mês
  - Região
  - Categoria/Produto
  - Canal/Vendedor

## 🗂️ Dados utilizados
Os dados estão disponíveis em: `dados/vendas_raw.csv`.

### Dicionário de dados
Consulte `dados/dicionario_de_dados.md` para entender o significado de cada coluna.

Exemplo de colunas esperadas:
- `Data`
- `PedidoID`
- `Produto` / `Categoria`
- `Regiao` / `Estado` / `Cidade`
- `Canal`
- `Quantidade`
- `PrecoUnitario`
- `Receita` (ou calculada como Quantidade * Preço)

## 🧠 Regras de negócio (cálculos)
- **Receita** = `Quantidade * PrecoUnitario` (se não existir pronta)
- **Ticket Médio** = `Receita Total / Nº de Pedidos`
- **Lucro** = `Receita - Custo` (se houver coluna de custo)
- **Margem (%)** = `Lucro / Receita`
