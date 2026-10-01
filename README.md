# Análise de contratações públicas

Este projeto analisa os objetos e os valores estimados de contratações públicas publicados no Portal Nacional de Contratações Públicas (PNCP). A coleta foi feita por meio da API, e os dados foram organizados para descrever os tipos de compras e a distribuição dos valores.

## Recorte da análise

- **Localidade:** São Paulo (SP)
- **Período pesquisado:** 1 a 15 de maio de 2025
- **Modalidade:** Pregão Eletrônico
- **Registros obtidos:** 1.429

As datas efetivamente encontradas nos registros vão de 2 a 14 de maio de 2025. A diferença em relação ao período pesquisado decorre dos dados retornados pela API.

## Arquivo

- `analise_contratacoes.ipynb`: notebook com a coleta, o tratamento, a classificação dos objetos e a análise exploratória.

## Como executar

1. Abra o notebook no [Google Colab](https://colab.research.google.com/) ou em um ambiente Jupyter.
2. Execute as células na ordem apresentada.
3. Quando solicitado, permita o acesso à internet para a consulta à API.

O notebook contém as etapas de coleta e análise. Como os dados disponíveis na API podem mudar, uma nova execução pode produzir resultados diferentes.

## Classificação dos objetos

Os objetos das contratações são agrupados em categorias temáticas com base em regras de texto descritas no notebook. Registros que não correspondem às regras definidas ficam em **“Outros”**. Essa categoria pode reunir objetos variados ou descrições que não foram reconhecidas pelas regras; portanto, sua frequência deve ser interpretada junto com essa limitação metodológica.

## Valores e boxplot

O boxplot aplica o critério de Tukey para identificar valores discrepantes. Esses valores permanecem nos dados e nos cálculos; os marcadores individuais de outliers podem ser ocultados no gráfico para facilitar a leitura. Valores iguais a zero são tratados separadamente quando o eixo está em escala logarítmica.

## Limitações

- A análise depende dos registros retornados pela API para os filtros definidos.
- A classificação temática depende das regras textuais implementadas no notebook.
- A categoria “Outros” não representa necessariamente uma categoria única de contratação.
- Os resultados descrevem o recorte analisado e não devem ser generalizados automaticamente para outros períodos ou localidades.

## Fonte dos dados

Portal Nacional de Contratações Públicas (PNCP) — dados obtidos por meio da API utilizada no notebook.

## Licença e uso

Este repositório disponibiliza o código para fins acadêmicos e de reprodutibilidade. Consulte os termos e as condições de uso dos dados na fonte oficial.
