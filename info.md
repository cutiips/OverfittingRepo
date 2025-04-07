## dataset

Prendre connaissance du dataset : https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview

_Note_ : Erreur logarithmique moyenne quadratique (askip c'est un truc important)

## consignes pour le projet

- vous incarnez une équipe de data scientists
- vous devez produire un use case réaliste avec le dataset à disposition (il faut produire un ML Canevas)
- vous devez tirer à travers toutes les étapes du CRISP-ML, exemple de la phase d'idéation jusqu'au déploiement (théorique)
- le déploiement correspond à la soumission de notre modèle ML sur kaggle.com
- vous devez rendre un Jupyter Notebook contenant votre code ainsi qu'une documentation exhaustive expliquant comment vous êtes arrivés à ce modèle.

## timeline suggérée

Phase de projet/planning conseillé sur la fin du semestre : 0. Phase zéro

1. Phase d'idéation
2. Phase de design
3. Evaluation et Blueprint
4. Rendu

### phase zéro

Produire un use case. Commencer par former les équipes (✅ fait) et produire un use case réaliste avec les dataset à disposition. Remplir le ML Canvas de manière aussi détaillé que possible.

Lien utile : https://ml-ops.org/content/phase-zero

### phase d'idéation

**Data Analysis et Data Mining**
Analysez les données en votre possession. Emettez des hypothèses sur les données qui possèdent le plus d'information selon vous. Créez un modèle baseline avec quelques variables sélectionnées par vos soins. Justifiez le raisonnement qui vous a conduit à ce modèle.

Lien utile : https://ml-ops.org/content/crisp-ml

### phase de design

**Data Engineering**
Préparez un Scikit-learn pipeline afin de traiter les données du dataset train et test. La pipeline doit être capable de `fit()` sur le dataset `train.csv` et `transform()`sur le dataset `test.csv`.

**Model Engineering**
Testez des modèles pertinents pourr votre use case. Les hyperparamètres doivent être ajustés. La performance des modèles est estimée indépendamment de la soumission sur kaggle. Le modèle est interprété à la lumière de votre compréhension du métier.

Lien utile : https://ml-ops.org/content/crisp-ml

### phase d'évaluation

**Evaluate**
Sélectionnez le modèle que vous estimez être le plus approprié pour votre use case. Discutez les raisons pour lesquelles vous avez sélectionné ce modèle et interprétez son fonctionnement sur votre dataset. Discutez l'efficacité et les limites du modèle pour votre business case. Préparez la pipeline complète à déployer (preprocessing et modèle), `fit()`sur le `train.csv`et `predict()`sur le `test.csv`.

Lien utile : https://ml-ops.org/content/crisp-ml

### blueprint et operation phase

**ML en production**
Soumettez vos résultats kaggle, reportez vos résultats dans le Jupyter Notebook et documentez votre code afin de raconter une histoire. Vous devez convaincre le management que votre solution va fonctionner en production. Discutez comment vous allez maintenir et monitorez l'algorithme ainsi que recueillir le feedback de vos utilisateurs. Finalement, discutez des potentiels implications éthiques et légales de votre solution.

Lien utile : https://ml-ops.org/content/mlops-principles

## ressources

- Nommer le notebook : GroupeCode-Nom1_Nom2_nom3.ipynb

### arborescence

```markdown
Overfittingrepo
│ .gitignore
│ 03-Marquis_Aris_Curty.ipynb
│ info.md
│ readme.md
├───data/
│ ├── data_description.txt
│ ├── sample_submission.csv
│ ├── test.csv
│ └── train.csv
└───doc/
├── 01-Introduction.pdf
├── 02-Supervised.pdf
├── 03-Ensemble Modeling.pdf
├── 04-Overfitting.pdf
├── 05-Control Overfitting.pdf
├── 06-CRISP-ML.pdf
├── 07-Project Kick-Off.pdf
├── 08-Performance.pdf
├── 09-Hyperparameter Tuning.pdf
├── 10-Epilogue.pdf
├── 11-Unsupervised.pdf
├── 12-Deep Learning.pdf
└── 13-Large Language Models.pdf
```
