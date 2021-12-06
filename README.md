# Trabalho 02 Unidade 01
Aluno: Pedro Cardoso Carvalho
## Dados 
Os dados foram obtidos pelo processo mostrado no repositorio https://github.com/alvarofpp/dataset-flights-brazil, com a substituição do arquivo transfom_to_graphml.py por o presente nesse repositorio. Substituição realizada para adicionar a caracteristi de região para o nós e realizar a filtragem dos dados para apenas de aeroportos e voos do Brasil. O resultado do processo está presente no arquivo air_traffic_brazil.graphml.

## Problemas e Analises 
Todos as soluções estão presente no notebook Solution.ipynb
### Estudo da assortatividade pela região
#### Problema 
-  Realizar um estudo sobre a
assortatividade da rede
considerando como atributo a
REGIÃO onde está localizado o
aeroporto.
-  Gerar um gráfico de conexões entre aerportos considerando como grupo a
REGIÃO.
#### Meotodologia 
Utilizando a função attribute_assortativity_coefficient da biblioteca networkx temos o coeficiente representativo da assossiatividade e utilizando CircosPlot da biblioteca nxviz conseguimos contruir o grafico de conexões entre os aeroportos.

### Análise bivariada entre o grau do vértice e o número médio de vizinhos
#### Problema
-  Gerar um gráfico de correlação
considerando a rede do
Brasil e de todas as
Regiões (Norte, Nordeste,
Sul, Sudeste e
Centro-Oeste).
-  Fazer um relato dos
principais achados. 
#### Metodologia
Utilizando a função degree_assortativity_coefficient da biblioteca networkx temos a correlação entre o grau do vértice e o número médio de vizinhos. Para construção do grafico temo a obtenção dos dados a partir da iteração com a função average_degree_connectivity da biblioteca networkx  e as bibliotecas plotly e seaborn para construção do grafico de correlação.

### Análise dos componentes da rede
#### Problema
-  Quantos componentes conectados existem na malha aérea
brasileira?(Caracterize cada componente: quantidade, porcentagem por
região)

#### Metodologia
Utilizando as funções number_connected_components e connected_components da biblioteca networkx foi possivel obter a quantidade de componentes da rede e realizar uma listagens dos nós presente. A partir disso realizei , utilizando o artificio de um dataframe auxiliar criado com as informações de cada aeroporto, a coleta dos dados e caracteristicas de cada componente.

### Simulação de Viagem
#### Problema
-  Crie um cenário simulado, onde se deseja fazer uma
viagem com o seguinte trajeto:
    - aeroporto 1 (Norte) para aeroporto 2 (Sul)
    - aeroporto 2 (Sul) para aeroporto 3 (Nordeste)
    - aeroporto 3 (Nordeste) para aeroporto 4(Centro-Oeste)
    - aeroporto 4 (Centro-Oeste) para aeroporto 5 (Sudeste)

#### Metodologia
Utilizando as funções shortest_path e shortest_path_length da biblioteca networkx foi possivel obter a rota de menor distancia entre dois aeroportos e a distancia dessa rota.
