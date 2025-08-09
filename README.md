# Simulação do Modelo de Ising com Machine Learning

Este projeto implementa uma simulação do Modelo de Ising e aplica técnicas de Machine Learning, inspirado por estudos que exploram o uso de aprendizado de máquina para identificar fases da matéria. O Modelo de Ising, um modelo fundamental em física estatística para o estudo do ferromagnetismo, é simulado e analisado.

Artigo reproduzido https://www.nature.com/articles/nphys4035.pdf

## Implementação do Modelo de Ising

A simulação do Modelo de Ising é realizada utilizando o algoritmo de Metropolis, otimizado para eficiência computacional.

As principais bibliotecas utilizadas são:

* `numpy`: Para operações numéricas e manipulação de arrays.
* `matplotlib`: Para geração de visualizações gráficas.
* `numba`: Para otimizar a performance da simulação com compilação JIT. 
* `pandas`: Para estruturar e salvar os dados gerados pela simulação. 

O código implementa a simulação do Modelo de Ising com otimizações para melhorar a velocidade de execução. O algoritmo de Metropolis é utilizado para simular as interações entre os spins.

## Machine Learning para Análise de Fase

Técnicas de Machine Learning, especificamente redes neurais, são empregadas para identificar as fases do Modelo de Ising, similar à abordagem de reconhecimento de padrões em transições de fase.

###   Arquitetura da Rede Neural

O modelo de rede neural é construído com `tensorflow.keras` e possui a seguinte arquitetura:

* Camada de entrada: Recebe os dados da simulação do Modelo de Ising. 
* Camada densa (1): Camada oculta com 100 neurônios e função de ativação sigmoid. 
* Camada densa (saída): Camada de saída com 2 neurônios e função de ativação sigmoid, adequada para classificação binária das fases.

###   Treinamento e Avaliação

O modelo é treinado utilizando o otimizador Adam e a função de perda BinaryCrossentropy. A acurácia é utilizada como métrica de avaliação durante o treinamento.

O desempenho do modelo é avaliado utilizando um conjunto de dados de teste, fornecendo métricas de perda e acurácia. 

## Resultados

Os resultados do treinamento do modelo, incluindo a acurácia e a perda ao longo das épocas, são visualizados para analisar o desempenho do aprendizado.

