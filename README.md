# Étude de marché internationale

## Contexte

La Poule qui Chante, entreprise spécialisée dans l’élevage et la vente de poulets bio, souhaite se développer à l’international.

L’objectif du projet est d’identifier des marchés présentant un potentiel de développement, à partir d’une analyse de données multi-pays.

## Données

Les données proviennent principalement de la **FAO** (*Food and Agriculture Organization*).

Les indicateurs utilisés couvrent notamment :

- la population ;
- la disponibilité alimentaire ;
- la production ;
- les importations et exportations, en valeur et en volume ;
- le PIB et son évolution ;
- la stabilité politique.

Plusieurs fichiers ont été nettoyés, pivotés puis fusionnés afin d’obtenir un jeu de données unique par pays et par année.

Les pays présentant des données manquantes, une stabilité politique inférieure à -1 ou des valeurs atypiques significatives ont été retirés. Le jeu de données final comprend **129 pays**.

## Démarche

Le projet a été réalisé avec **Python**.

Des indicateurs complémentaires ont été calculés, notamment :

- la croissance de la population sur cinq ans ;
- le PIB par habitant ;
- le taux de dépendance aux importations ;
- la valeur unitaire des importations.

L’analyse s’est déroulée en plusieurs étapes :

1. nettoyage et fusion des données ;
2. contrôle des valeurs manquantes et des outliers ;
3. analyse en composantes principales (ACP) ;
4. classification hiérarchique ascendante (CAH) ;
5. segmentation des pays avec K-Means.

L’ACP a permis de résumer les données autour de trois axes principaux :

- la taille et le volume du marché ;
- le niveau de développement économique ;
- l’intégration dans le commerce international.

## Résultats

La segmentation K-Means a permis d’identifier cinq groupes de pays :

- marchés émergents ;
- marchés stables et développés ;
- marchés matures et diversifiés ;
- grands pays industriels ;
- grands marchés en développement.

Les pays européens du même cluster que la France, considérés comme les marchés les plus proches du positionnement recherché, sont :

- Espagne ;
- Royaume-Uni ;
- Italie ;
- Roumanie ;
- Pologne.

D’autres marchés européens stables et développés ont également été identifiés, dont le Portugal, l’Irlande, la Suisse, la Suède et la Norvège.

## Limites et pistes d’amélioration

L’étude repose sur des données agrégées par pays. Elle ne prend pas directement en compte certains critères propres au marché du poulet bio, comme la réglementation locale, les habitudes de consommation, la concurrence ou les circuits de distribution.

Pour aller plus loin :

- intégrer des données spécifiques au marché du bio ;
- ajouter une analyse de la concurrence locale ;
- étudier les contraintes réglementaires par pays ;
- compléter la segmentation avec des données sur les prix et les comportements d’achat.

## Outils utilisés

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
