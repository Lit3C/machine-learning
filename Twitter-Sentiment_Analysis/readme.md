Entraîne-toi à classifier des tweets pour dire s'ils sont positifs ou négatifs. Ca pourrait être un outil très utile pour optimiser le travail d'un community manager.

1.   Importe l'ensemble de données de tweets [**train.csv**](https://github.com/Lit3C/machine-learning/blob/main/Twitter-Sentiment_Analysis/train.csv) dans un DataFrame.
2.   Ne garde que les tweets positifs et négatifs (tu excluras donc les `neutral`). Quel est le pourcentage de tweets positifs/négatifs ?
3.   Copie la colonne `text` dans une Série `X`, et la colonne `sentiment` dans une Série `y`. Applique un train test split avec le `random_state = 32` et un `train_size` de 0.75.
4.   Crée un modèle `vectorizer` avec scikit-learn en utilisant la méthode `Countvectorizer`. Entraîne ton modèle sur `X_train`, puis crée une matrice de features `X_train_CV`. Crée la matrice `X_test_CV` sans ré-entraîner le modèle. Le format de la matrice `X_test_CV` doit être `4091x15806` avec `44633 stored elements`.
5.   Entraîne maintenant une régression logistique avec les paramètres par défaut. Tu devrais obtenir les résultats suivants : `0.966` pour le test d'entraînement, et `0.877` pour l'ensemble de test.
6.   Étape bonus : essaye d'afficher 10 tweets qui ont été mal prédits (faux positifs ou faux négatifs). Aurais-tu fait mieux que l'algorithme ?