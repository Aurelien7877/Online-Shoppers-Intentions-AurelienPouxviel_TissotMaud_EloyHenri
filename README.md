# Online-Shoppers-Intentions-AurelienPouxviel_TissotMaud_EloyHenri
Projet de python A4 DIA par Maud Tissot, Henri Eloy et Aurélien Pouxviel - 

Online Shoppers Purchasing Intention Dataset
Résumé : Sur les 12 330 sessions de l'ensemble de données, 84,5 % (10 422) étaient des échantillons de classe négative qui ne se terminaient pas par des achats, et le reste (1908) était des échantillons de classe positive se terminant par des achats.

## But : Analyser les données, les transformer et prédire si oui ou non une session peut mener à un achat (variable 'Revenue' 0 ou 1)

# I - Data PreProcessing

Pour résumé, dans cette première partie, nous avons exploré tout le dataset. D'abord nous avons expliqué les différents attributs, puis nous avons fait une succession de plot univarié pour mieux les comprendre.
Ensutie, nous avons transformer nos données. Nous avons encoder les variables non numérique, puis également d'autres variable numérique en hot encode.
Dans la partie prédiction nous avons standriser nos données.

# II - Analyse des données
  ## Analyse des correlations
  
Dans cette seconde partie, nous avons analysé les données en bivariées et multivariées, toujours en lien avec notre target 'Revenue'.
Nous avons d'abord calculer les corrélations de chaque variable, y compris celle crées, avec notre target. Cela nous a fait ressortir les variables les plus corrélées.

  ## Analyses Bivariées / Multivariées
  
Ici nous avons réalisé de nombreuses analyses bivariées et multivariées.
  - Le type de page visitée selon l'aboutissement de l'achat
  - La durée de visite d'une page selon le type de page et selon l'aboutissement de l'achat
  - Special day et Revenue
  - Bounce Rate et Revenue
  - Exit Rate et Revenue
  - ExitRates en fonction de BounceRates et Revenue
  - Pages Values par type de page et Revenue
  - Weekend et mois de l'année avec Revenue

Ces analyses ont confirmé l'impact, en plus de la corrélation, sur notre target Revenue

# III - Modelisation de l'intention d'achat : Machine Learning + Deep Learning
  ## Test de diffèrents modèles et interpretation
  ## Comparaison des modèles
  ## Deep Learning
  
# IV - Transformation du modèle en API
