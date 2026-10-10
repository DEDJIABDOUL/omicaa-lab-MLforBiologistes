# Données

Aucune donnée brute volumineuse n'est versionnée dans ce dépôt. Les notebooks récupèrent les données de façon reproductible, au moment de l'exécution.

## Projet fil rouge : Breast Cancer Wisconsin (Diagnostic)

* **Contenu** : 569 observations, 30 caractéristiques numériques calculées à partir d'images de ponction à l'aiguille fine de masses mammaires, un diagnostic (maligne ou bénigne). Aucune valeur manquante.
* **Origine** : UCI Machine Learning Repository, jeu n° 17. Wolberg W. H., Street W. N., Mangasarian O. L. Breast Cancer Wisconsin (Diagnostic). DOI : https://doi.org/10.24432/C5DW2B
* **Licence** : Creative Commons Attribution 4.0 International (CC BY 4.0), d'après la page UCI du jeu de données.
* **Accès dans les notebooks** : `sklearn.datasets.load_breast_cancer`, copie intégrée à scikit-learn, aucun téléchargement nécessaire.
* **Limite** : cette copie ne contient pas d'identifiant patient. L'indépendance des observations ne peut pas être vérifiée.
* **Codage de la cible** : scikit-learn code 0 pour maligne et 1 pour bénigne. Les notebooks recodent la cible pour que la classe positive soit la tumeur maligne.

## Projet intégrateur : leucémies de Golub et al. (1999)

* **Contenu** : 72 échantillons (47 ALL, 25 AML), 7129 sondes Affymetrix.
* **Publication d'origine** : Golub T. R. et al. Molecular classification of cancer: class discovery and class prediction by gene expression monitoring. Science 286(5439):531-537, 1999.
* **Source utilisée par le notebook 07** : copie publique sur GitHub, `https://raw.githubusercontent.com/ramhiser/datamicroarray/master/data/golub.RData`, mise en cache dans `data/cache/` à l'exécution.
* **Somme de contrôle SHA-256 du fichier utilisé** : `594f5507597fb2352d210c803a88a218fbf6d1f2705372029e5738815216747b` (1 191 760 octets).
* **Licence** : **non vérifiée** pour cette copie. Vérifier les conditions de redistribution avant toute réutilisation hors du cadre pédagogique, et citer la publication d'origine.
* **Pourquoi pas NCBI GEO ou UCI** : ces serveurs étaient inaccessibles depuis l'environnement dans lequel les notebooks ont été validés (HTTP 403). Le notebook 07 propose, en exercice d'extension, de reproduire la démarche sur une série GEO officielle.
* **Limites** : pas d'annotation des sondes (aucun nom de gène n'est affirmé), pas de métadonnées d'échantillons (centre, tissu, sexe).

## Données simulées et fictives

Certains notebooks construisent de petits jeux **synthétiques** à des fins pédagogiques (table fictive du notebook 03, valeurs manquantes simulées du notebook 02, patients simulés du notebook 05). Ils sont toujours signalés comme tels et ne représentent aucune donnée réelle.
