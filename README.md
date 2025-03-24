# Simulação do Modelo de Ising com Machine Learning

Este projeto implementa uma simulação do Modelo de Ising e aplica técnicas de Machine Learning, inspirado por estudos que exploram o uso de aprendizado de máquina para identificar fases da matéria. O Modelo de Ising, um modelo fundamental em física estatística para o estudo do ferromagnetismo, é simulado e analisado.

## Implementação do Modelo de Ising

A simulação do Modelo de Ising é realizada utilizando o algoritmo de Metropolis, otimizado para eficiência computacional.

As principais bibliotecas utilizadas são:

* `numpy`: Para operações numéricas e manipulação de arrays. [cite: 13, 14, 2, 3, 4, 5, 6, 8]
* `matplotlib`: Para geração de visualizações gráficas. [cite: 13, 3, 9, 17]
* `numba`: Para otimizar a performance da simulação com compilação JIT. [cite: 13, 4]
* `pandas`: Para estruturar e salvar os dados gerados pela simulação. [cite: 13, 5, 3]

O código implementa a simulação do Modelo de Ising com otimizações para melhorar a velocidade de execução. O algoritmo de Metropolis é utilizado para simular as interações entre os spins. [cite: 13, 14, 2]

## Machine Learning para Análise de Fase

Técnicas de Machine Learning, especificamente redes neurais, são empregadas para identificar as fases do Modelo de Ising, similar à abordagem de reconhecimento de padrões em transições de fase.

###   Arquitetura da Rede Neural

O modelo de rede neural é construído com `tensorflow.keras` e possui a seguinte arquitetura:

* Camada de entrada: Recebe os dados da simulação do Modelo de Ising. [cite: 16, 17, 4, 5]
* Camada densa (1): Camada oculta com 100 neurônios e função de ativação sigmoid. [cite: 16, 17, 5]
* Camada densa (saída): Camada de saída com 2 neurônios e função de ativação sigmoid, adequada para classificação binária das fases. [cite: 16, 18, 6]

###   Treinamento e Avaliação

O modelo é treinado utilizando o otimizador Adam e a função de perda BinaryCrossentropy. A acurácia é utilizada como métrica de avaliação durante o treinamento. [cite: 18, 19, 6]

O desempenho do modelo é avaliado utilizando um conjunto de dados de teste, fornecendo métricas de perda e acurácia. [cite: 16, 20, 21, 6]

## Resultados

Os resultados do treinamento do modelo, incluindo a acurácia e a perda ao longo das épocas, são visualizados para analisar o desempenho do aprendizado. [cite: 20, 21, 7, 8, 9]

## Como Executar

Para executar este projeto, certifique-se de ter o Python 3.x instalado e as bibliotecas necessárias.

1.  Clone este repositório.
2.  Instale as dependências utilizando `pip install -r requirements.txt` ou instale as bibliotecas individualmente.
3.  Execute o script principal para simular o Modelo de Ising e treinar o modelo de Machine Learning.

```bash
python seu_script.py
