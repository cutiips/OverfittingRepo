# Cas d’usage : Estimation automatisée du prix de vente d’une maison sur une plateforme en ligne

## Description du problème métier

La mise en vente d’un bien immobilier s’accompagne d’une question critique : **à quel prix le proposer sur le marché ?** Fixer un prix de vente adéquat est un défi pour les propriétaires et les professionnels. Un prix trop élevé peut dissuader les acheteurs et allonger inutilement la durée de vente, tandis qu’un prix sous-évalué fait perdre de la valeur au vendeur.

Actuellement, l’estimation repose souvent sur l’expertise d’agents immobiliers ou sur la comparaison manuelle avec des ventes récentes similaires. Ce processus peut être long, subjectif et inégal d’un expert à l’autre.

Dans ce contexte, imaginons une plateforme de vente immobilière en ligne souhaitant améliorer son service en offrant aux particuliers un **outil d’estimation automatique** du prix de leur maison. Le problème métier à résoudre est clair : fournir une évaluation fiable, rapide et objective de la valeur d’un bien immobilier afin d’aider le propriétaire à prendre la bonne décision.

En proposant une estimation instantanée dès la mise en vente, la plateforme vise à :

- Rassurer les vendeurs sur le juste prix à afficher.
- Réduire les allers-retours liés aux négociations ou aux avis d’experts multiples.

Ce cas d’usage est tout à fait réaliste – de grands acteurs du secteur immobilier utilisent déjà ce type d’outils pour apporter de la valeur ajoutée à leurs clients (par exemple, des sites web offrent des estimations gratuites en ligne, incitant les propriétaires à engager leurs services).

---

## Rôle des données dans ce contexte

Les **données historiques de ventes immobilières** sont au cœur de la solution. Elles servent de base pour entraîner un modèle de machine learning capable de prédire le prix de vente à partir des caractéristiques d’un bien.

Par exemple, le dataset Kaggle _“House Prices: Advanced Regression Techniques”_ fournit 79 variables décrivant presque tous les aspects d’une maison (superficie, nombre de pièces, type de construction, année de construction, état général, quartier, etc.) ainsi que son prix de vente final. Ce jeu de données détaillé est représentatif des informations nécessaires : il permet de capturer les facteurs qui influencent la valeur d’un bien et d’apprendre la relation entre ces facteurs et le prix.

Une estimation fiable requiert d’analyser une multitude de données pertinentes :

- Attributs propres au bien (taille, âge, caractéristiques internes).
- Contexte de vente (localisation, quartier, ventes récentes comparables, tendances du marché immobilier local, etc.).

Dans notre cas d’usage, toutes ces données alimentent le modèle de prédiction. Concrètement, la plateforme en ligne disposerait d’une base de données d’historique de ventes (issues soit de ses propres transactions passées, soit de données publiques/open data immobilières).

Le modèle de ML va apprendre sur ces exemples historiques :

- Découvrir la plus-value apportée par une chambre supplémentaire.
- Comprendre l’impact moyen d’un garage.
- Identifier la décote liée à un vieux logement non rénové.

Plus le volume et la qualité des données sont élevés, plus le modèle sera performant pour estimer de nouveaux biens. _(À noter : il est important d’actualiser régulièrement les données pour que le modèle reste à jour des évolutions du marché.)_

---

## Acteurs concernés

Plusieurs acteurs sont impliqués et bénéficient d’une telle solution d’estimation automatisée :

1. **Propriétaires vendeurs (particuliers)**

   - Utilisateurs finaux de l’outil d’estimation en ligne.
   - Ils renseignent les caractéristiques de leur logement sur la plateforme et obtiennent immédiatement une fourchette de prix estimative.
   - Cela les aide à décider d’un prix de mise en vente réaliste et à gagner en confiance dans le processus.

2. **Plateforme immobilière en ligne (entreprise)**

   - Acteur qui met en place le service.
   - L’outil d’estimation sert à attirer de nouveaux vendeurs sur son site (_génération de leads_) et à les convertir en clients.
   - L’entreprise y voit un avantage concurrentiel en se positionnant comme un service innovant et transparent.

3. **Agents immobiliers / conseillers de l’entreprise**

   - Si la plateforme collabore avec des agents immobiliers, ces professionnels utilisent également l’estimation automatique comme aide à la décision.
   - Par exemple, un agent peut s’appuyer sur le prix suggéré par le modèle lors de ses discussions avec le vendeur, afin de justifier le prix conseillé avec des données à l’appui.

4. **Équipe Data Science / IT**
   - Data scientists et ingénieurs ML développent, entraînent et mettent à jour le modèle de prédiction.
   - Ils veillent à la qualité des données, à la performance du modèle et à son intégration dans la plateforme en ligne.

_(Acteurs indirects : les acheteurs potentiels, qui bénéficieront in fine de prix plus justes sur le marché, bien qu’ils n’interagissent pas directement avec le modèle.)_

---

## Impact du modèle ML dans le processus métier

### Intégration dans le processus actuel

L’introduction d’un modèle de Machine Learning va transformer la façon dont l’estimation de prix est réalisée au sein du processus de vente.

- **Avant le modèle ML** :
  Le propriétaire contacte un agent ou évalue de lui-même, un rendez-vous d’estimation est planifié, l’agent analyse le bien et les comparables manuellement, puis propose un prix estimé après quelques heures ou jours.
  _Ce processus traditionnel est chronophage et mobilise des ressources humaines pour chaque nouvelle propriété._

- **Avec le modèle ML** :
  Le propriétaire entre les informations clés sur son bien (surface, nombre de chambres, adresse, etc.) dans un formulaire web.
  Instantanément, le modèle calcule une estimation de la valeur marchande en se basant sur les données et tendances apprises.
  _Exemple : « Maison estimée à 250 000 € (fourchette 240 000 € – 260 000 €) »._

### Gains concrets apportés par la solution ML

1. **Rapidité et efficacité** :
   Le délai pour obtenir une estimation passe de plusieurs jours à quelques secondes.

2. **Homogénéité et objectivité** :
   Chaque bien est évalué selon les mêmes critères _data-driven_, éliminant en partie les biais ou variations d’un estimateur à l’autre.

3. **Amélioration de la précision globale** :
   L’algorithme détecte des patterns complexes qu’un humain moyen ne pourrait pas prendre en compte entièrement.

4. **Évolution continue** :
   Le modèle peut être mis à jour périodiquement avec de nouvelles données de ventes conclues, afin d’affiner ses prédictions.

---

## Objectifs métiers du projet

1. **Attirer et convertir davantage de clients vendeurs** :
   En offrant une estimation gratuite et instantanée, la plateforme génère du trafic et des leads qualifiés.

2. **Optimiser le positionnement des biens sur le marché** :
   Fixer dès le départ un prix de vente juste et compétitif augmente les chances de vente rapide.

3. **Maximiser la satisfaction client et la confiance** :
   Savoir que le prix proposé est étayé par des données robustes améliore l’image de la plateforme.

4. **Gagner en efficacité interne et réduire les coûts** :
   Automatiser la première phase d’estimation permet de diminuer le temps de travail humain consacré aux évaluations préliminaires.

5. **Valoriser les données et innover dans le secteur** :
   Ce projet dote la plateforme d’une compétence clé en science des données, ouvrant la voie à d’autres services innovants.

---

En résumé, ce cas d’usage de prédiction du prix des maisons apporte une solution concrète à un problème métier courant dans l’immobilier. Il exploite la richesse des données disponibles pour apporter rapidité, précision et objectivité au processus d’estimation, au bénéfice de tous les acteurs impliqués.
