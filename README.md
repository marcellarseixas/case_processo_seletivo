
# 📦 iFood Case – Análise de Campanha com Cupons

Este projeto realiza uma análise de viabilidade de campanhas de cupons no iFood, utilizando PySpark e ferramentas estatísticas para avaliar o impacto da ação em diferentes segmentos de usuários.

## 📋 Premissas

- O iFood está **financiando o custo total do cupom**.
- O valor do cupom **não está descontado no valor do pedido** — a coluna `discount` está zerada para todos os pedidos.
- Existem `order_id` duplicados com datas diferentes. Considerou-se que são pedidos distintos, sendo criada uma coluna auxiliar concatenando `order_id` + `order_created_at`.

## ⚙️ Requisitos

Para rodar o notebook, é necessário ter instalado:

- Python ≥ 3.8
- Apache Spark (recomendado via `pyspark`)
- Pacotes Python:
  ```bash
  pip install pyspark pandas matplotlib seaborn scikit-learn statsmodels scipy
  ```

## 🚀 Como Executar

1. Clone este repositório ou baixe o notebook `Case_Marcella_Ifood_final_real.ipynb`.
2. Certifique-se de ter o Apache Spark configurado localmente ou use uma plataforma como Google Colab com suporte ao PySpark.
3. Execute as células do notebook em sequência.
4. Os principais passos executados são:

   - 📥 Leitura e tratamento dos dados
   - 🔍 Análise descritiva e de comportamento dos usuários
   - 🧪 Teste A/B (controle vs target)
   - 🧠 Segmentação de usuários com KMeans (MiniBatchKMeans)
   - 📊 Avaliação de performance da campanha e sugestões estratégicas

## 📈 Output Esperado

- Visualizações de comportamento por cluster
- Cálculo de ROI estimado
- Sugestões personalizadas de campanha por grupo

## 📁 Estrutura Esperada de Dados

O notebook utiliza arquivos `.csv` compactados `.tar.gz`. Certifique-se de ter os dados em um diretório acessível e ajustar os caminhos conforme necessário.

## 💻 Execute no Google Colab

Você pode executar diretamente no Google Colab clicando abaixo:

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)
