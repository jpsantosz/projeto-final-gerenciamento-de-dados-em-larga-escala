# 🎮 Análise de Reviews da Steam com PySpark

Projeto final da disciplina de Gerenciamento de Dados em Larga Escala que explora análise de sentimentos em reviews de jogos da plataforma Steam utilizando PySpark, MLlib e visualizações com Matplotlib.

## 📊 Descrição do Projeto

Este projeto realiza uma análise abrangente de reviews de jogos da Steam, explorando padrões de satisfação dos jogadores, identificando jogos mais populares e criticados, e comparando o desempenho de processamento entre Pandas e Spark em grandes volumes de dados.

### 🎯 Objetivos

- Analisar mais de 1 milhão de reviews de jogos da Steam
- Identificar padrões de sentimento (positivo/negativo) nos reviews
- Comparar desempenho de processamento entre Pandas e Spark
- Visualizar insights através de gráficos informativos
- Demonstrar aplicação prática de conceitos de Big Data

## 🗂️ Estrutura do Dataset

**Fonte:** [Steam Reviews Dataset](https://www.kaggle.com/datasets/andrewmvd/steam-reviews)

**Estrutura:**
```
+------+--------------+--------------------+------------+------------+
|app_id|      app_name|         review_text|review_score|review_votes|
+------+--------------+--------------------+------------+------------+
|    10|Counter-Strike|     Ruined my life.|           1|           0|
|    10|Counter-Strike|This will be more...|           1|           1|
+------+--------------+--------------------+------------+------------+
```

**Campos:**
- `app_id`: ID único do jogo na Steam
- `app_name`: Nome do jogo
- `review_text`: Texto do review
- `review_score`: Sentimento (1 = positivo, -1 = negativo)
- `review_votes`: Número de votos úteis no review

**Volume:** ~1.3 milhões de reviews de 9.000+ jogos

## 🛠️ Tecnologias Utilizadas

- **PySpark 3.5.0** - Processamento distribuído de dados em larga escala
- **Python 3.12** - Linguagem de programação
- **Matplotlib & Seaborn** - Visualização de dados
- **Google Colab** - Ambiente de desenvolvimento
- **Google Drive** - Armazenamento do dataset

## 📈 Análises Realizadas

### 1. Análise Exploratória
- Estatísticas gerais do dataset (total de reviews, jogos únicos)
- Distribuição de sentimentos (positivos vs negativos)
- Identificação dos jogos mais reviewados

### 2. Top 100 Jogos Mais Reviewados
- Ranking dos 100 jogos com maior volume de reviews
- Análise de distribuição de reviews por jogo

### 3. Análise de Sentimento
- Proporção geral de reviews positivos vs negativos
- Taxa de aprovação por jogo
- Identificação de jogos mais bem e mal avaliados

### 4. Análises Específicas

#### 📊 Visualizações Criadas:

1. **Gráfico de Pizza - Distribuição Geral**
   - Proporção de reviews positivos vs negativos no dataset completo
   - Percentuais e valores absolutos

2. **Top 10 Jogos com Mais Reviews**
   - Gráfico de barras horizontais
   - Volume total de reviews por jogo

3. **Análise de Sentimento - Top 10**
   - Comparação de reviews positivos e negativos
   - Percentuais de aprovação/rejeição

4. **Top 10 Jogos Mais Criticados**
   - Jogos com maior número absoluto de reviews negativos
   - Comparação com reviews positivos

5. **Top 10 Maior Taxa de Rejeição**
   - Jogos com maior porcentagem de reviews negativos (mínimo 100 reviews)
   - Identificação de jogos mais mal avaliados proporcionalmente

## 📊 Principais Resultados

### Estatísticas Gerais
- **Total de reviews analisados:** ~1.3 milhões
- **Jogos únicos:** 9.000+
- **Taxa de aprovação geral:** ~75-80% de reviews positivos
- **Top 100 jogos:** Concentram mais de 60% do total de reviews

### Insights Descobertos

1. **Concentração de Reviews:**
   - Os top 10 jogos representam uma parcela significativa do volume total
   - Jogos populares como PAYDAY 2, DayZ e Terraria dominam o ranking

2. **Padrões de Sentimento:**
   - Maioria dos jogos tem aprovação positiva (>70%)
   - Jogos com muitos reviews tendem a ter melhor equilíbrio entre positivos/negativos
   - Alguns jogos específicos apresentam taxa de rejeição >85%

3. **Performance Spark vs Pandas:**
   - Spark demonstra vantagens em operações de agregação complexas
   - Para o volume de dados analisado, ambas tecnologias são viáveis
   - Spark escala melhor para datasets maiores

## 🎓 Conceitos de Big Data Aplicados

### Volume
- Processamento de milhões de registros de reviews
- Dataset com múltiplas dimensões (texto, metadados, scores)

### Variedade
- Dados estruturados (scores, IDs, votes)
- Dados não estruturados (texto dos reviews)

### Velocidade
- Comparação de performance entre frameworks
- Otimização de queries para grandes volumes

### Veracidade
- Filtragem de dados inconsistentes (valores nulos)
- Validação de review_scores
- Limpeza de registros duplicados

### Valor
- Insights sobre satisfação dos jogadores
- Identificação de padrões de sucesso/fracasso
- Base para recomendações e análises futuras
---

**Data:** Dezembro 2024  
**Disciplina:** Gerenciamento de Dados em Larga Escala  
**Ferramentas:** PySpark 3.5.0, Python 3.12, Matplotlib, Google Colab
