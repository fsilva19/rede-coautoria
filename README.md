# Redes Temporais de Co-Autoria (U1P1)
---
Disciplina: Algoritmos e Estruturas de Dados II
</br>Discente: Felipe Gabriel B. da Silva

---
</br>
O presente projeto tem como objetivo analisar a rede de co-autoria dos trabalhos do Programa de Pós-graduação em Engenharia Elétrica e de Computação (PPgEEC) da UFRN, bem como reforçar os conceitos sobre grafos aprendidos em sala de aula, utilizando a biblioteca NetworkX. 
</br>
Outras bibliotecas importantes que também são utilizadas no projeto:

*   Matplotlib
*   Google.colab
*   Joypy
*   Seaborn
*   Pandas

# Requisito 1
## Análise do comportamento na série temporal anual.
Métricas analisadas:
*   Densidade da rede 
*   Número de vértices (nós)
*   Número de arestas (conexões)
*   Número médio de vizinhos
*   Distribuição do número de vizinhos

Foram criadas 5 listas para guardar os valores das métricas, a fim de facilitar o uso dos valores no futuro. Para isso, foram utilizadas as seguintes funções da biblioteca NetworkX:
*   G = nx.read_gexf()
*   nx.density(G)
*   G.number_of_nodes()
*   G.number_of_edges()
*   G.degree()

```
Rede de autores de 2010
Densidade: 0.032, Nº de nós: 276, Nº de arestas: 1227, Grau médio: 8.891

Rede de autores de 2011
Densidade: 0.031, Nº de nós: 306, Nº de arestas: 1451, Grau médio: 9.484

Rede de autores de 2012
Densidade: 0.034, Nº de nós: 280, Nº de arestas: 1324, Grau médio: 9.457

Rede de autores de 2013
Densidade: 0.029, Nº de nós: 366, Nº de arestas: 1928, Grau médio: 10.536

Rede de autores de 2014
Densidade: 0.026, Nº de nós: 437, Nº de arestas: 2439, Grau médio: 11.162

Rede de autores de 2015
Densidade: 0.027, Nº de nós: 415, Nº de arestas: 2285, Grau médio: 11.012

Rede de autores de 2016
Densidade: 0.032, Nº de nós: 375, Nº de arestas: 2214, Grau médio: 11.808

Rede de autores de 2017
Densidade: 0.028, Nº de nós: 411, Nº de arestas: 2366, Grau médio: 11.513

Rede de autores de 2018
Densidade: 0.026, Nº de nós: 460, Nº de arestas: 2773, Grau médio: 12.057

Rede de autores de 2019
Densidade: 0.021, Nº de nós: 605, Nº de arestas: 3887, Grau médio: 12.850

Rede de autores de 2020
Densidade: 0.023, Nº de nós: 532, Nº de arestas: 3186, Grau médio: 11.977

Rede de autores de 2021
Densidade: 0.024, Nº de nós: 541, Nº de arestas: 3489, Grau médio: 12.898

Rede de autores de 2022
Densidade: 0.024, Nº de nós: 571, Nº de arestas: 3982, Grau médio: 13.947

Rede de autores de 2023
Densidade: 0.023, Nº de nós: 570, Nº de arestas: 3786, Grau médio: 13.284

Rede de autores de 2024
Densidade: 0.025, Nº de nós: 552, Nº de arestas: 3811, Grau médio: 13.808

Rede de autores de 2025
Densidade: 0.093, Nº de nós: 135, Nº de arestas: 841, Grau médio: 12.459
```
# Gráfico comparativo
A partir dos dados acima, foi possível criar um gráfico mostrando a evolução das métricas das redes de co-autoria do PPgEEC.
*   No eixo X estão setados os anos das redes (2010 até 2025).
*   No eixo Y estão os valores de cada uma das métricas em escala logarítimica.

Foi utilizada a escala logarítimica no eixo Y em razão da diferença de escala das métricas, para fins de comparação.
</br>Os gráficos abaixo foram criados utilizando funções da biblioteca Matplotlib.
</br>Foram criadas linhas verticais representando marcos importantes das avaliações do PPgEEC nos anos de 2012, 2016, 2020 e 2024.

![IMG1](https://github.com/user-attachments/assets/bc359221-31c8-4f83-93de-459ec570c0c1)

# Gráfico comparativo
Um segundo modelo de gráfico foi criado para melhor visualização das métricas, a fim de serem analisadas de forma individual.
</br>Da mesma maneira, foram criados marcos importantes referentes às avaliações do PPgEEC nos anos de 2012, 2016, 2020 e 2024.

![IMG2](https://github.com/user-attachments/assets/21f5e7c5-a92a-44fc-8cbb-d2ae2a06c0c1)

## Histograma - Função de densidade de probabilidade
A fim de ser analisada a distribuição do número de vizinhos nas redes, foi criado um histograma para visualizar como o grau dos nós evolui ao longo dos anos.
</br>
</br>Utilizando a biblioteca Joypy, foi criado um gráfico do tipo Ridge Plot, um estilo de gráfico em 'camadas', a fim de analisar o comportamento da curva de probabilidade dos graus de cada rede.

```
pip install joypy # Para instalar a biblioteca Joypy
```

![IMG3](https://github.com/user-attachments/assets/35c88232-1395-44e5-ad8e-3e76a181065c)

# Requisito 2
# Visualização dos Grafos
### Foi criado um grafo para cada período de avaliação do PPgEEC, a fim de serem visualizadas as conexões e características das redes.
#### Períodos de avaliação:


1.   2010 até 2012
2.   2013 até 2016
3.   2017 até 2020
4.   2021 até 2025

#### Características importantes dos grafos:
*   O tamanho do vértice é proporcional ao número de vizinhos (grau do vértice)
*   Os 5 vértices com mais vizinhos estão destacados com a cor vermelha e é mostrado o valor do 'id'
*   Cor da aresta dependerá da ligação entre membros permanentes:
  *   vermelha, caso a propriedade do vértice 'is_permanent' = True
  *   Preta, caso a propriedade do vértice 'is_permanent' = False
*   A espessura da aresta será proporcional à quantidade de citações:
  *   Ou seja, proporcional à propriedade da aresta 'citation_num'

![IMG4](https://github.com/user-attachments/assets/76eb2a53-2633-44d1-b596-0da38485a3b8)
![IMG5](https://github.com/user-attachments/assets/dd8d27a3-6f32-4d8e-9034-4cdf323ab713)
![IMG6](https://github.com/user-attachments/assets/c0f89729-9c2f-4aa1-80c5-3613a38b8577)
![IMG7](https://github.com/user-attachments/assets/89e3e9cc-322b-4e8f-8d21-575360ce3a62)

# Requisito 3
## Rede Geral
O código abaixo cria um grafo com os dados da rede geral (2010-2025) de co-autoria do PPgEEC, mantendo as mesmas características do requisito 2. 
A fim de análise, são impressas as métricas da rede, mostrando a Densidade, nº de  nós, nº de arestas e média dos graus.

```
Rede de autores geral (2010-2025)
Densidade: 0.009, Nº de nós: 2454, Nº de arestas: 26113, Grau médio: 21.282
```
![IMG8](https://github.com/user-attachments/assets/1b75bed0-c4f5-480d-8eea-566807079401)

Nessa segunda parte do requisito 3, é criado um sub-grafo da rede geral apenas com os vértices que possuem pelo menos 200 vizinhos. 
</br>A fim de análise, são impressas as métricas da rede, mostrando a Densidade, Nº de  nós, Nº de arestas e Média dos graus.

```
Sub-grafo da rede geral de autores
Densidade: 0.561, Nº de nós: 19, Nº de arestas: 96, Grau médio: 10.105
```
![IMG9](https://github.com/user-attachments/assets/e9e3ee51-542e-4431-9074-f0e160b5d337)

```
Nó Ego de maior grau do sub-grafo
Densidade: 0.590, Nº de nós: 15, Nº de arestas: 62, Grau médio: 8.267
```
![IMG10](https://github.com/user-attachments/assets/7f7bd2b0-15d3-436a-8d7f-64245cbed041)

