# ✈️ Análise de Lucratividade de Rotas Aéreas

##  Visão Geral

Este projeto apresenta uma análise exploratória sobre a lucratividade de rotas aéreas utilizando **PySpark** em ambiente **Databricks**.

O objetivo é identificar os principais fatores que influenciam a rentabilidade das operações aéreas a partir de um conjunto de dados contendo informações de receitas, custos operacionais, demanda, ocupação e características das aeronaves.

Além da análise de negócio, o projeto demonstra um fluxo de preparação e enriquecimento de dados utilizando tecnologias amplamente empregadas em ambientes corporativos de engenharia e análise de dados.

---

## Objetivos

Responder às seguintes questões de negócio:

- Quais fatores estão mais associados à lucratividade das rotas?
- Como a estrutura de custos impacta o resultado financeiro?
- Existe relação entre a taxa de ocupação (Load Factor) e a margem de lucro?
- Como o tipo de aeronave influencia a eficiência operacional?

---

## Tecnologias Utilizadas

- Python
- PySpark
- Databricks
- Spark SQL
- Git
- GitHub

---

## Dataset

Fonte:

https://www.kaggle.com/datasets/waleedfaheem/airline-route-profitability-and-cost-analysis

O conjunto de dados contém 7.974 registros, incluindo informações como:

- Origem e destino
- Tipo de aeronave
- Capacidade da aeronave
- Número de passageiros
- Taxa de ocupação (Load Factor)
- Horas de voo
- Receita com passagens
- Receita acessória (Ancillary Revenue)
- Receita total
- Custos operacionais detalhados
- Lucro
- Margem de lucro

---

## Fluxo do Projeto

O projeto foi desenvolvido seguindo um fluxo semelhante ao utilizado em projetos reais de Analytics.

```
Dataset Kaggle
        │
        ▼
Catálogo do Databricks
        │
        ▼
Leitura dos dados (PySpark)
        │
        ▼
Validação da qualidade dos dados
        │
        ▼
Feature Engineering
        │
        ▼
Análise Exploratória
        │
        ▼
Geração de Insights
```

---

## Etapas Desenvolvidas

### 1. Data Understanding

- Leitura da tabela no Catálogo do Databricks
- Verificação do schema
- Estatísticas descritivas
- Identificação de valores nulos
- Verificação de registros duplicados

---

### 2. Feature Engineering

Foram criadas novas métricas de negócio para enriquecer a análise:

- Profitability
- Profit Per Hour
- Revenue Per Passenger
- Cost Per Passenger
- Profit Per Passenger

---

### 3. Análise Exploratória

Foram realizadas análises sobre:

- Estrutura dos custos operacionais
- Correlação entre variáveis
- Lucratividade por categoria
- Eficiência operacional das aeronaves

---

## Principais Resultados

### Receita por passageiro é o principal fator associado à lucratividade

As rotas classificadas como **High** apresentaram uma receita média por passageiro aproximadamente **2,5 vezes superior** às rotas classificadas como **Loss**.

Os resultados indicam que a capacidade de gerar receita possui impacto significativamente maior sobre a lucratividade do que pequenas reduções nos custos operacionais.

---

### A ocupação influencia a margem, mas não explica sozinha a lucratividade

Foi observada uma correlação positiva entre Load Factor e Profit Margin, indicando que voos com maior ocupação tendem a apresentar melhores resultados financeiros.

Entretanto, essa relação mostrou-se moderada, sugerindo que outros fatores, como receita por passageiro e estrutura de custos, possuem maior influência sobre a rentabilidade.

---

### Aeronaves de grande porte apresentaram maior eficiência operacional

No conjunto de dados analisado, aeronaves como Airbus A380 e Boeing 777-300ER apresentaram maiores valores médios de:

- Profit Per Hour
- Profit Margin
- Profit Per Passenger

Os resultados sugerem que a maior receita gerada por passageiro foi suficiente para compensar seus custos operacionais mais elevados.

---

### Estrutura dos custos

As maiores parcelas do custo operacional foram:

| Categoria | Participação Média |
|------------|-------------------:|
| Sales Distribution Cost | 18,36% |
| Fuel Cost | 17,56% |
| Overhead Cost | 15,70% |
| Depreciation Cost | 10,13% |

Essas quatro categorias representam a maior parte do custo operacional observado no dataset.

---

## Análises Realizadas

- Estrutura percentual dos custos
- Matriz de correlação
- Heatmap de correlação
- Comparação entre níveis de lucratividade
- Eficiência operacional por tipo de aeronave

---

## Principais Insights

- Receita por passageiro apresentou maior influência sobre a lucratividade do que o custo por passageiro.
- Voos com maior ocupação tendem a apresentar maiores margens de lucro, embora a ocupação não seja o único fator determinante.
- A eficiência operacional, medida pelo lucro por hora voada, apresentou diferenças significativas entre os grupos de lucratividade.
- A maior parte dos custos operacionais concentra-se em poucas categorias, principalmente custos de distribuição, combustível e despesas administrativas.

---

## Limitações

Este projeto utiliza um conjunto de dados público desenvolvido para fins educacionais.

Dessa forma, algumas características observadas podem não representar fielmente a realidade da indústria da aviação.

Um exemplo identificado durante a análise foi que aeronaves amplamente utilizadas comercialmente, como o Airbus A320 e o Boeing 737-800, apresentaram margem média negativa.

Na prática, esses modelos são reconhecidos por sua elevada eficiência operacional e econômica em operações de curta e média distância, sendo amplamente utilizados por companhias aéreas em todo o mundo.

Portanto, as conclusões relacionadas ao desempenho financeiro de tipos específicos de aeronaves devem ser interpretadas apenas no contexto deste dataset e não generalizadas para operações reais.

Outra limitação importante é a ausência de informações sobre horários de partida e chegada dos voos, impossibilitando análises relacionadas aos períodos do dia.

---

## Possíveis Evoluções

Este projeto pode ser expandido com novas análises, como:

- Dashboard interativo em Power BI
- Modelos preditivos para previsão de lucro
- Clusterização de rotas

---

## Autor

**Arthur Maldonado**

Graduado em Aviação Civil e cursando MBA em Data Science & Analytics.

Projeto desenvolvido com foco em demonstrar habilidades em Analytics utilizando PySpark e Databricks.
