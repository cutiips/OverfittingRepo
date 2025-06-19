
# Cas d’usage : Estimation automatique du prix de vente pour une plateforme immobilière en ligne

## Problème métier

L’objectif principal de notre plateforme est de permettre à un **propriétaire particulier** souhaitant vendre son bien de connaître immédiatement une **estimation objective de son prix**. Cette estimation permet :

* D’instaurer **confiance** chez le vendeur.
* De **réduire les délais de vente** en affichant un prix réaliste dès le départ.
* D’**automatiser** le processus pour limiter la mobilisation de ressources humaines coûteuses.

Dans ce cadre, nous intégrons un **modèle de machine learning** directement dans notre interface, permettant à l’utilisateur d’obtenir une **estimation instantanée** dès qu’il renseigne les caractéristiques de son bien.

---

## Rôle des données

Le jeu de données Kaggle *House Prices: Advanced Regression Techniques* constitue une base réaliste pour construire ce système :

* Il contient **79 variables descriptives** (superficie, nombre de pièces, quartier, qualité des matériaux, etc.) et un prix de vente final.
* Il reflète fidèlement les données que notre plateforme peut collecter via un formulaire rempli par l’utilisateur.

Ces données seront utilisées pour entraîner notre modèle à **prédire un prix à partir de caractéristiques connues**. Pour rester fiable, le modèle sera mis à jour régulièrement avec **de nouvelles ventes enregistrées** sur la plateforme.

---

## Acteurs concernés

1. **Vendeurs particuliers**

   * Utilisent l’outil pour obtenir une estimation fiable et gratuite.
   * Décident ensuite de mettre leur bien en ligne avec plus de sérénité.

2. **Plateforme**

   * Propose une **expérience utilisateur innovante**.
   * Génère des leads qualifiés via l’usage de l’outil d’estimation.
   * Réduit les allers-retours de négociation.

3. **Équipe Data Science**

   * Conçoit, teste, valide et surveille le modèle.
   * S’appuie sur le cycle **CRISP-ML** pour garantir la robustesse et l’évolutivité du système.

---

## Intégration du modèle dans le processus métier

* Avant : le vendeur doit consulter un agent ou faire une estimation manuelle via comparaison ou intuition.
* Après : en quelques clics, il renseigne les informations sur son bien et obtient une **fourchette de prix automatisée** (ex. : "entre 260 000 € et 280 000 €").

Cela améliore l’expérience client, limite les frictions et **valorise la data comme avantage compétitif**.

---

## Objectifs business

| Objectif                              | Description                                                                          |
| ------------------------------------- | ------------------------------------------------------------------------------------ |
| Générer des leads                     | En fournissant une estimation gratuite, on attire des vendeurs sur notre plateforme. |
| Réduire les délais de vente           | Un bon positionnement tarifaire favorise une vente rapide.                           |
| Augmenter la satisfaction utilisateur | En proposant un outil rapide et fiable.                                              |
| Réduire les coûts internes            | Moins de besoins d’agents ou d’experts mobilisés.                                    |
| Innover et se différencier            | Proposer un service basé sur des techniques de machine learning modernes.            |

---

## Approche ML envisagée

1. **Modèles testés** : Régressions (linéaire, Lasso, Ridge), Arbres de décision, Random Forest, Gradient Boosting, XGBoost.
2. **Pipeline** : Nettoyage, encodage, normalisation, sélection de features.
3. **Évaluation** : RMSE, RMSLE (notamment car recommandé pour ce challenge).
4. **Validation croisée** : Utilisation de K-Fold pour limiter l’overfitting.
5. **Hyperparamètres** : Grid Search, Random Search ou méthode bayésienne selon le modèle.

---

## Étapes CRISP-ML suivies

| Phase                  | Action                                                                                                               |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Idéation**           | Compréhension du problème métier et de l’opportunité commerciale.                                                    |
| **Data Understanding** | Exploration des variables les plus informatives (ex. : quartier, superficie, qualité).                               |
| **Design**             | Création d’un pipeline sklearn prêt à transformer `train.csv` et `test.csv`.                                         |
| **Model Engineering**  | Test de plusieurs modèles et tuning des hyperparamètres.                                                             |
| **Evaluation**         | Sélection du meilleur modèle pour la plateforme, interprétation métier.                                              |
| **Operation**          | Soumission sur Kaggle, puis intégration potentielle dans la plateforme avec monitoring, MLOps et contrôle de dérive. |

---

## Conclusion

Notre use case illustre une **application concrète du machine learning au service du business**. Grâce à l’outil d’estimation :

* Le vendeur bénéficie d’un service rapide, fiable et rassurant.
* La plateforme optimise son acquisition client et ses performances internes.
* Le modèle peut évoluer avec les tendances du marché et rester pertinent.

