# Redes Temporais de Co-Autoria (U1P1)
---
Disciplina: Algoritmos e Estruturas de Dados II
</br>Discente: Felipe Gabriel B. da Silva

---
</br>
O presente projeto tem como objetivo analisar a rede de co-autoria dos trabalhos do Programa de Pós-graduação em Engenharia Elétrica e de Computação (PPgEEC) da UFRN, bem como reforçar os conceitos sobre grafos, aprendidos em sala de aula, utilizando a biblioteca NetworkX. 
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
