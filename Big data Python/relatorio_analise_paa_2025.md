# Relatório de Análise de Dados - PAA 2025

## 1. Introdução

Este trabalho apresenta uma análise exploratória de dados relacionada ao Programa de Aquisição de Alimentos (PAA) de 2025. O objetivo principal foi entender como os consumidores do programa se distribuem entre diferentes tipos de atendimento, identificando padrões de concentração, relevância relativa e possíveis desigualdades na participação das categorias analisadas.

A análise foi desenvolvida em Python, com apoio das bibliotecas `pandas`, `matplotlib` e `seaborn`, permitindo tanto o tratamento dos dados quanto a geração de estatísticas descritivas e visualizações gráficas.

## 2. Objetivo da análise

O notebook tem como foco responder, de forma organizada, às seguintes perguntas:

1. Quantos consumidores existem em cada tipo de categoria?
2. Qual é a participação percentual de cada tipo em relação ao total?
3. Quais categorias concentram maior volume de atendimento?
4. A distribuição dos consumidores é equilibrada ou concentrada em poucos grupos?

Essas perguntas orientam a leitura dos dados e ajudam a transformar a tabela original em uma interpretação útil para apresentação acadêmica.

## 3. Fonte e preparação dos dados

Na primeira etapa, o notebook carrega um arquivo Excel com os dados do programa. A leitura é feita automaticamente a partir do arquivo encontrado na pasta de trabalho. Em seguida, o conjunto de dados é convertido em um DataFrame do `pandas`, permitindo a exploração das colunas e dos registros.

Depois do carregamento, o trabalho realiza um ajuste de nomenclatura: a coluna `Tipo Consumidor.Tipo Consumidor` é renomeada para `Tipo Consumidor`, o que facilita a leitura e a manipulação posterior.

Essa etapa de preparação é importante porque reduz ruídos no tratamento dos dados e deixa o conjunto mais adequado para análise e visualização.

## 4. Análise exploratória inicial

A análise começa com uma inspeção geral do DataFrame, incluindo:

1. Visualização das primeiras linhas.
2. Verificação da estrutura do conjunto de dados.
3. Cálculo de estatísticas descritivas.
4. Conferência de valores ausentes.

Esse tipo de exploração é essencial para entender o comportamento dos dados antes de criar indicadores derivados. A partir das estatísticas apresentadas no notebook, é possível observar que a variável `Qtd Consumidor` apresenta média de 4,86 e mediana de 2, indicando que a maior parte das categorias possui valores mais baixos, enquanto poucas categorias concentram quantidades maiores.

O desvio padrão de 5,05 reforça essa ideia de dispersão considerável entre as categorias.

## 5. Criação da métrica percentual

Uma das contribuições mais importantes do trabalho foi a criação da coluna `Percentual Consumidor`. Essa métrica foi calculada com base na quantidade total de consumidores, usando a seguinte lógica:

\[
\text{Percentual Consumidor} = \frac{\text{Qtd Consumidor}}{\text{Total de Consumidores}} \times 100
\]

Essa transformação é relevante porque permite comparar categorias em termos proporcionais, e não apenas em valores absolutos. Em muitas análises, o número bruto pode esconder a real representatividade de cada grupo. Ao converter para percentual, a leitura se torna mais clara e interpretável.

Depois disso, o notebook organiza uma tabela com as colunas `Tipo Consumidor`, `Qtd Consumidor` e `Percentual Consumidor`, ordenada do maior para o menor percentual. Isso destaca rapidamente os grupos mais representativos no programa.

## 6. Visualização dos dados

O trabalho também inclui gráficos de barras para facilitar a comunicação dos resultados:

1. Um gráfico com a quantidade de consumidores por tipo.
2. Um gráfico com o percentual de consumidores por tipo.

Essas visualizações ajudam a perceber visualmente a concentração dos valores. Em vez de apenas ler a tabela, o leitor consegue identificar rapidamente quais categorias dominam a distribuição.

O uso de gráficos horizontais melhora a legibilidade, principalmente quando os nomes das categorias são longos, como ocorre neste conjunto de dados.

## 7. Estatísticas descritivas adicionais

Após a criação da nova variável percentual, o notebook calcula estatísticas descritivas específicas para `Qtd Consumidor` e `Percentual Consumidor`.

Os principais resultados descritos no próprio trabalho são os seguintes:

1. Média de `Qtd Consumidor`: 4,86.
2. Mediana de `Qtd Consumidor`: 2.
3. Desvio padrão de `Qtd Consumidor`: 5,05.
4. Média de `Percentual Consumidor`: 14,29%.
5. Mediana de `Percentual Consumidor`: 5,88%.
6. Desvio padrão de `Percentual Consumidor`: 14,85%.
7. Valor mínimo observado: 1 consumidor, equivalente a 2,94%.
8. Valor máximo observado: 15 consumidores, equivalente a 44,12%.

Esses números indicam forte assimetria na distribuição. A média maior do que a mediana sugere que poucas categorias possuem valores altos o suficiente para puxar o comportamento geral para cima.

## 8. Interpretação dos resultados

A leitura combinada das estatísticas e dos gráficos mostra que o Programa de Aquisição de Alimentos apresenta uma distribuição heterogênea entre os tipos de consumidores.

Isso significa que o atendimento não está igualmente distribuído entre todas as categorias. Em vez disso, há forte concentração em alguns grupos, especialmente em entidades de assistência social e na rede pública de educação, citadas no próprio notebook como categorias de maior peso.

Do ponto de vista analítico, essa concentração pode ser interpretada de três maneiras principais:

1. Pode refletir maior capacidade de captação e atendimento por parte de algumas instituições.
2. Pode indicar que a demanda está concentrada em determinados perfis de beneficiários.
3. Pode revelar oportunidade de ampliar o alcance em categorias com menor participação.

Assim, o trabalho não apenas descreve os dados, mas também ajuda a levantar hipóteses sobre a distribuição dos recursos e a cobertura do programa.

## 9. Conclusão

De forma geral, a análise mostra que o PAA 2025 atende a diferentes tipos de consumidores, mas com distribuição desigual entre as categorias. O uso da variável percentual foi fundamental para revelar a representatividade real de cada grupo dentro do total de atendimentos.

O estudo cumpre bem o papel de uma análise exploratória inicial: organiza os dados, cria uma métrica comparativa, produz visualizações e oferece uma interpretação clara sobre a concentração observada.

Como conclusão prática, o trabalho demonstra que poucas categorias concentram uma parcela significativa dos consumidores, enquanto várias outras têm participação menor. Isso fornece uma base útil para decisões futuras, planejamento de políticas públicas e aprofundamento da análise em trabalhos posteriores.

## 10. Sugestões de melhoria

Para evoluir o trabalho, seria interessante:

1. Incluir análise por região, município ou período, se essas variáveis existirem no arquivo original.
2. Comparar os resultados de 2025 com anos anteriores.
3. Investigar se há correlação entre tipo de consumidor e volume de atendimento.
4. Exportar os resultados finais em PDF ou HTML para apresentação.

Esses próximos passos tornariam o estudo mais robusto e ajudariam a transformar a análise descritiva em uma investigação mais estratégica.