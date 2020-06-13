# Projeto de Aprendizagem Automática II

## Procura de Exoplanetas no Espaço através da Emissão de Luz de Estrelas

O <a href="https://www.kaggle.com/keplersmachines/kepler-labelled-time-series-data">conjunto de dados</a> descreve as alterações no *flux*, ou seja, na intensidade da luz de milhares de estrelas. Desta forma, cada estrela possui um rótulo binário de valor 1 ou 2. O rótulo 2 indica que a estrela tem garantidamente pelo menos um exoplaneta em órbita, sendo que existem sistemas multi-planeta. No que toca ao rótulo 1, este indica a não existência de exoplanetas na órbita da estrela.

Como é sabido, os planetas por si não emitem luz, mas sim as estrelas nas quais orbitam. Assim, se uma determinada estrela for observada durante vários meses ou anos, pode existir um "escurecimento" regular do *flux*, podendo isto indicar que podem existir corpos a orbitar no sistema. Desta forma, este sistema torna-se candidato a mais análise, podendo ser alvo de estudo extra com auxílio de um satélite que captura luz num comprimento de onda diferente. Este estudo pode solidificar as indicações de que o sistema pode possuir exoplanetas, confirmando até esta crença.  

Assim, os dados em estudo foram tratados a partir de observações feitas pelo telescópio *Kepler* da NASA. A Missão chegou ao seu fim no dia 30 de outubro de 2018, sendo substituída por outras semelhantes. No que toca aos dados, mais de 99% são originários da Campanha número 3. De modo a aumentar o número de exoplanetas confirmados, foram incluídas observações de outras campanhas. Quer isto dizer que além da inclusão de todas as observações da Campanha 3, foram também incluídos registos de estrelas com exoplanetas em órbita descobertas em outras campanhas. Segundo os autores do conjunto de dados, a escolha da 3ª Campanha baseou-se nesta aparentar não possuir classificações erradas de exoplanetas.

Além disso, os dados originais da Missão *Kepler* estão armazenados no Arquivo Mikulski, sendo parte dos dados *open-source* da NASA. É importante mencionar que após o regresso à Terra, a NASA aplica algoritmos de remoção de ruído para eliminar artefactos gerados pelo próprio telescópio. 

### Objetivos

Como se trata de um problema de classificação, o grande objetivo deste projeto é a classificação correta do maior número de casos possível. No entanto, tendo em conta a diferença nas quantidades de dados de cada classe, é extremamente importante classificar corretamente os casos referentes à classe minoritária, de modo a evitar _overfitting_ nos modelos. Para isso, serão testados métodos de _Machine Learning_, bem como de _Deep Learning_, sendo, posteriormente, efetuada uma otimização de hiperparâmetros dos melhores modelos na tentativa de obtenção de melhores resultados. 

### Notebooks

* [Exploração, Visualização e Tratamento dos Dados](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/EDA/eda.ipynb)
* [Modelos de Machine Learning](https://github.com/citoplasme/Automatic_Learning_2/tree/master/Modelos/ML/)
  * [Não Supervisionados](https://github.com/citoplasme/Automatic_Learning_2/tree/master/Modelos/ML/Nao_Supervisionados)
    * [K Means Clustering](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Nao_Supervisionados/K_Means_Clustering/k_means.ipynb)
    * [Spectral Clustering](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Nao_Supervisionados/Spectral_Clustering/spectral_clustering.ipynb)
  * [Supervisionados](https://github.com/citoplasme/Automatic_Learning_2/tree/master/Modelos/ML/Supervisionados)
    * [SVM](https://github.com/citoplasme/Automatic_Learning_2/tree/master/Modelos/ML/Supervisionados/SVM)
      * [SVM Base](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Supervisionados/SVM/svm.ipynb)
      * [SVM com Otimização de Hiperparâmetros](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Supervisionados/SVM/svm_otimizacao.ipynb)
    * [KNN com Distância de Minkowski](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Supervisionados/KNN/Minkowski/knn_minkowski.ipynb)
    * [Random Forest](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Supervisionados/Random_Forest/random_forest.ipynb) 
    * [Classificador SGD com Otimização de Hiperparâmetros](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Supervisionados/SGDClassifier/sgdclassifier_otimizacao.ipynb)
* [Modelos de Deep Learning](https://github.com/citoplasme/Automatic_Learning_2/tree/master/Modelos/DL)
  * [RNN](https://github.com/citoplasme/Automatic_Learning_2/tree/master/Modelos/DL/RNN/)
    * [LSTM](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/DL/RNN/LSTM)
      * [LSTM Base](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/DL/RNN/LSTM/LSTM.ipynb)
      * [LSTM com Otimização de Hiperparâmetros](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/DL/RNN/LSTM/lstm_otimizacao.ipynb)
  * [CNN](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/DL/CNN)
    * [CNN Base](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/DL/CNN/CNN.ipynb)
    * [CNN com Otimização de Hiperparâmetros](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/DL/CNN/cnn_otimizacao.ipynb)
  * [DNN](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/DL/DNN/DNN.ipynb)

### Conclusão

Este repositório representa o resultado do trabalho prático da unidade curricular de Aprendizagem Automática II, do perfil de Ciência de Dados. Neste contexto foram abordados os passos referentes ao desenvolvimento e implementação de vários modelos que permitissem a classificação de estrelas, com base na presença de exoplanetas na sua órbita, tirando proveito da linguagem de programação *Python* e as suas bibliotecas.

No que toca aos vários modelos testados, foi possível constatar a melhor *performance* vinda de modelos apropriados para problemas com variações temporais, tais como redes *LSTM*, redes convolucionais e até mesmo classificadores lineares. Infelizmente, fruto do grande desbalanceamento de dados, especialmente no conjunto de teste, torna-se complicado comparar modelos. No entanto, apesar deste problema, os modelos desenvolvidos apresentaram resultados bastante bons, sendo que a existência de mais registos ou a execução de um método de *leave one out cross validation* poderiam permitir a obtenção de melhores resultados. 

Além disso, não foi possível testar modelos com base em métricas de *Dynamic Time Warping*, sendo que estas poderiam trazer melhores análises dos dados, especialmente em contexto não supervisionado. Ainda sobre este, o desenvolvimento e teste de modelos com base em algoritmos alternativos poderia culminar em alguns resultados interessantes. 

Em suma, a realização deste trabalho exigiu a aplicação de todos os conhecimentos lecionados em contexto de aula, bem como a pesquisa de novos métodos, permitindo o desenvolvimento de modelos de *Machine* e *Deep Learning* capazes de produzir resultados satisfatórios para o problema em questão.
