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
* [Modelos de Machine Learning](https://github.com/citoplasme/Automatic_Learning_2/edit/master/modelos/ML/)
  * [Não Supervisionados](https://github.com/citoplasme/Automatic_Learning_2/edit/master/modelos/ML/Nao_Supervisionados)
    * [K Means Clustering](https://github.com/citoplasme/Automatic_Learning_2/edit/master/modelos/ML/Nao_Supervisionados/K_Means_Clustering)
  * [Supervisionados](https://github.com/citoplasme/Automatic_Learning_2/edit/master/modelos/ML/Supervisionados)
    * [SVM](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Supervisionados/SVM/svm.ipynb)
    * [KNN com Distância Euclidiana](https://github.com/citoplasme/Automatic_Learning_2/blob/master/Modelos/ML/Supervisionados/KNN/Euclidian/knn_euclidian.ipynb)
* [Modelos de Deep Learning](https://github.com/citoplasme/Automatic_Learning_2/edit/master/modelos/DL/)
  * [RNN](https://github.com/citoplasme/Automatic_Learning_2/edit/master/modelos/DL/RNN)
    * [LSTM](https://github.com/citoplasme/Automatic_Learning_2/edit/master/modelos/DL/RNN/LSTM/lstm.ipynb)
  * [CNN](https://github.com/citoplasme/Automatic_Learning_2/edit/master/modelos/DL/CNN/cnn.ipynb)
