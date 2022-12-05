# Online-Shoppers-Intentions-AurelienPouxviel_TissotMaud_EloyHenri
Projet de python A4 DIA par Maud Tissot, Henri Eloy et Aurélien Pouxviel - 

Online Shoppers Purchasing Intention Dataset
Résumé : Sur les 12 330 sessions de l'ensemble de données, 84,5 % (10 422) sont des échantillons de classe négative qui ne se terminent pas par un achats, et le reste (1908) sont des échantillons de classe positive se terminant par un achats.

## But : Analyser les données, les transformer et prédire si oui ou non une session mène à un achat (variable 'Revenue' 0 ou 1) et faire une api

# I - Data PreProcessing

Pour résumer, dans cette première partie, nous avons exploré tout le dataset. D'abord nous avons expliqué les différents attributs, puis nous avons fait une succession de plots univariés pour mieux les comprendre.
Ensuite, nous avons transformé nos données. Nous avons encodé les variables non numériques, puis également d'autres variables numériques en hot encoding.
Dans la partie prédiction nous avons standardisé nos données.

# II - Analyse des données
  ## Analyse des corrélations
  
Dans cette seconde partie, nous avons analysé les données en bivariée et multivariée, toujours en lien avec notre target 'Revenue'.
Nous avons d'abord calculé les corrélations de chaque variables, y compris celles créées, avec notre target. Ce qui nous a permis d'observer les variables les plus corrélées.

  ## Analyses Bivariées / Multivariées
  
Nous avons réalisé de nombreuses analyses bivariées et multivariées.
  - Le type de page visitée selon l'aboutissement de l'achat
  - La durée de visite d'une page selon le type de page et selon l'aboutissement de l'achat
  - Special day et Revenue
  - Bounce Rates et Revenue
  - Exit Rates et Revenue
  - ExitRates en fonction de BounceRates et Revenue
  - Page Values par type de page et de Revenue
  - Weekend et mois de l'année avec Revenue

Ces analyses ont confirmé l'impact, en plus de la corrélation, sur notre target Revenue

# III - Modelisation de l'intention d'achat : Machine Learning et Deep Learning
  ## Test de diffèrents modèles et interprétation

Nous avons utilisé nos 8 variables les plus corrélées pour effectuer une succession de modèles de machine learning (et deep learning plus tard).
Dans un premier temps, nous avons divisé notre dataset en X et Y, avec Y la variable à prédire. Ensuite nous avons standardisé notre X, puis divisé en train et en test nos données.

Chaque modèle que nous avons réalisés est hyperparamétré grâce à nos fonctions de gridsearch. Nous avons effectué en machine learning :
  - KNN
  - GAUSSIAN NAIVE BAYES
  - SVM
  - DECISION TREE
  - LOGISTIC REGRESSION
  - XGBOOST CLASSIFIER
  - RANDOM FOREST CLASSIFIER

  ## Comparaison des modèles
  
Pour chaque modèle nous calculons sa précision, différents scores comme le F1 score sur lequel nous nous basons pour choisir le meilleur modèle, sa matrice de confusion, et éventuellement sa ROC curves et un graphique d'importance des variables pour le random forest.

Enfin, nous avons dressé un tableau basé sur le F1-score qui classe nos modèles.

  ## Deep Learning

Nous avons réalisé 2 modèles de réseaux de neuronnes avec tensorflow et keras, un cas d'overfitting avec les 30 variables de notre dataset et un meilleur sans overfitting avec les 8 variables les plus correlées 
  
# IV - Transformation du modèle en API

Pour finir, nous avons implémenté notre code dans une api dans laquelle nous donnons 8 paramètres, ainsi que le choix d'un ou plusieurs modèles. Cette api retourne la prédiction par le modèle demandé.
