# Projeto de Análise de Dados

## 1. Objetivo
Aplicar os conhecimentos técnicos de forma prática, utilizando boas práticas de documentação, programação e organização, simulando uma situação real no âmbito empresarial e utilizando dados de vendas.

## 2. Ferramentas Utilizadas
* Linguagem de Programação: Python (Bibliotecas: Pandas, Seaborn e Matplotlib.pyplot)
* Dataset: Sample_Superstore (Dataset público disponível em https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
* Ambiente de Programação: Jupyter Notebook

## 3. Estrutura e Tratamento de Dados
O projeto foi dividido para separar a engenharia de dados da análise de negócios:

`tratamento_dataset.ipynb`: Focado na limpeza e preparação. As etapas incluíram:

- Verificação de Data Quality (remoção de duplicadas e tratamento de nulos).
- Tradução e padronização completa das colunas e dos registros (ex: Furniture para Mobília).
- Criação da métrica calculada Margem de Lucro %.

`graficos_plot.ipynb`: Focado na análise visual e resposta às perguntas de negócio.

`SampleSuperstore_Tratado.csv`: A base de dados final tratada e utilizada para as visualizações.

## 4. Análise Exploratória e Resultados
A investigação seguiu um raciocínio lógico (do macro para o micro), gerando as seguintes descobertas comprovadas pelos dados:

> I. Volume de Vendas por Categoria
O gráfico de barras demonstrou que a categoria de Tecnologia lidera o faturamento bruto da empresa, seguida de perto por Mobília e, por fim, Materiais de Escritório.

> II. Evolução do Lucro Anual
A análise temporal em gráfico de linhas confirmou uma trajetória positiva e de crescimento do negócio. O lucro total apresentou uma tendência de alta consistente entre os anos de 2014 e 2017.

> III. Margem de Lucro por Categoria
Apesar do alto volume de vendas identificado no primeiro gráfico, a análise de eficiência financeira revelou um cenário alarmante para a categoria de Mobília. A média de margem de lucro ficou distribuída da seguinte forma:
Tecnologia: 15.61%
Materiais de Escritório: 13.80%
Mobília: Apenas 3.88%

> IV. A Causa Raiz: Lucro vs. Desconto
Para investigar a baixa rentabilidade de certas vendas, o gráfico de dispersão cruzou o lucro absoluto com as faixas de desconto (0% a 80%). A inserção de uma linha de base (zero) evidenciou que descontos a partir de 20% arrastam massivamente as operações para a zona de prejuízo.

## 5. Recomendações à Gestão
Com base nos dados analisados, as recomendações estratégicas são:

- **Revisão da Política de Descontos:** Estabelecer um teto restrito de descontos. O limite de 20% mostrou-se o ponto de ruptura onde a operação deixa de ser financeiramente viável.

- **Reestruturação da Categoria de Mobília:** Sendo a segunda categoria que mais vende, mas com uma margem de apenas 3.88%, é urgente revisar custos de fornecedores, logística ou repassar reajustes de preços ao consumidor final.