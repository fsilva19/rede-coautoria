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
