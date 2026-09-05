# Relatório de Resultados — Adventure Works 2013

Dashboard em Excel alimentado por consultas SQL, desenvolvido a partir do curso **Hashtag Treinamentos** (SQL integrado ao Excel) e posteriormente refinado com melhorias próprias de visualização de dados.

![Dashboard final](imagens/dashboard_final.png)

## 🎯 Sobre o projeto

O objetivo foi extrair e tratar dados de vendas da base **Adventure Works** via SQL Server, trazer o resultado para o Excel e montar um dashboard executivo com os principais indicadores de 2013: receita, custo, sazonalidade de vendas, mix de categorias e distribuição por gênero.

Este projeto teve como ponto de partida o curso da Hashtag Treinamentos. A estrutura das consultas SQL segue o que foi ensinado no curso; as melhorias de visualização no dashboard (ordenação, formatação de rótulos, linha de tendência, substituição de gráficos pouco informativos) foram desenvolvidas por conta própria, aplicando boas práticas de storytelling de dados.

## 🛠️ Tecnologias

- **SQL Server** — extração e tratamento da base Adventure Works
- **Excel** — modelagem de tabelas, fórmulas e construção do dashboard

## 📁 Estrutura do repositório

```
├── sql/
│   └── consultas_adventure_works.sql   # scripts de extração e tratamento
├── excel/
│   └── dashboard_adventure_works_2013.xlsx
├── imagens/
│   ├── dashboard_original.png          # versão inicial (do curso)
│   └── dashboard_final.png             # versão com melhorias aplicadas
└── README.md
```

## 📊 O dashboard

O painel reúne quatro blocos de análise:

1. **Receita Total vs. Custo Total por País** — comparativo entre os 6 principais mercados
2. **Vendas por Mês** — evolução mensal de unidades vendidas ao longo de 2013
3. **Vendas por Categoria** — participação de Accessories, Bikes e Clothing no total
4. **Vendas por Gênero** — distribuição entre público feminino e masculino

## ✨ Melhorias aplicadas em relação à versão original

| Item | Antes | Depois | Por quê |
|---|---|---|---|
| Rótulos de dado | Valores completos (R$ 4.339.443) | Formato abreviado (R$ 4,3M) | Reduz poluição visual e facilita leitura rápida |
| Ordenação dos países | Alfabética | Decrescente por Receita | Identifica os principais mercados de imediato, sem precisar comparar barra por barra |
| Vendas por mês | Barras simples | Barras + linha de tendência/média móvel, com destaque no mês de pico | Evidencia a sazonalidade (queda em jan/fev, pico em dez) que ficava escondida nos números brutos |
| Vendas por categoria | Gráfico de pizza | Barras horizontais | Comparação de proporções é mais precisa em barras do que em ângulos, especialmente com só 3 categorias |
| Vendas por gênero | Gráfico de rosca (donut) | Cartões de KPI diretos | A diferença entre os grupos é de apenas 0,14 p.p. — praticamente um empate. Um gráfico circular sugere uma diferença visual que não existe nos dados; cartões com o número exato comunicam isso com mais honestidade |

## 📚 Créditos

Projeto desenvolvido durante o curso **SQL + Excel** da [Hashtag Treinamentos](https://www.hashtagtreinamentos.com/), com a base de dados de exemplo **Adventure Works** (Microsoft). As consultas SQL seguem a estrutura ensinada no curso; as decisões de design do dashboard e as melhorias de visualização foram desenvolvidas de forma independente, como exercício de aprofundamento em storytelling de dados.

## 🚀 Aprendizados

- Como estruturar consultas SQL para alimentar diretamente um modelo de dados no Excel
- Critérios para escolher o tipo de gráfico certo para cada tipo de comparação (categórica, temporal, parte-todo)
- A importância de formatar rótulos e ordenar dados pensando em quem vai *ler* o dashboard, não só em quem o construiu
