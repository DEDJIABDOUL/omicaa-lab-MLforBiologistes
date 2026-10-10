# Omicaa Lab | Machine Learning et Deep Learning pour les biologistes

**De la donnée brute au modèle prédictif reproductible.** Auteur : DEDJI ABDOUL BATINOU. Marque éditoriale : Omicaa Lab.

Dispositif de formation autonome comprenant un ebook PDF d'environ 30 pages, sept notebooks Jupyter exécutables dans Google Colab et ce dépôt. L'apprenant construit progressivement un système prédictif à partir de données biologiques, depuis les premières lignes de Python jusqu'à un projet intégrateur sur des données d'expression génique.

> **Statut de publication.** Ce dépôt a été préparé localement. Les liens Colab ci-dessous pointent vers le chemin prévu `github.com/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics` (branche `main`) et ne fonctionneront qu'après publication. Les notebooks n'ont pas été testés dans Google Colab lui-même.

## Objectifs

À l'issue du parcours, l'apprenant sait examiner un jeu de données inconnu, définir une question prédictive, construire un pipeline sans fuite d'information, comparer des modèles à un modèle de référence, optimiser des hyperparamètres sans toucher au test, évaluer avec des métriques justifiées, sauvegarder et recharger un modèle, et distinguer performance prédictive, association statistique et conclusion biologique.

## Prérequis

Aucun prérequis informatique. Des connaissances élémentaires de biologie et de statistiques descriptives suffisent. Un compte Google pour Colab, ou un environnement Python 3.10 ou supérieur.

## Parcours

| Notebook | Contenu | Ouvrir dans Colab |
|---|---|---|
| 01 Python fondamentaux | variables, fonctions, FASTA, exceptions | [ouvrir](https://colab.research.google.com/github/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics/blob/main/notebooks/01_python_fondamentaux.ipynb) |
| 02 NumPy, pandas, exploration | tableaux, DataFrames, contrôle qualité | [ouvrir](https://colab.research.google.com/github/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics/blob/main/notebooks/02_numpy_pandas_exploration.ipynb) |
| 03 Visualisation et prétraitement | figures, valeurs atypiques, partitionnement, fuite | [ouvrir](https://colab.research.google.com/github/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics/blob/main/notebooks/03_visualisation_et_pretraitement.ipynb) |
| 04 Classification et pipelines | modèle de référence, 4 algorithmes, métriques | [ouvrir](https://colab.research.google.com/github/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics/blob/main/notebooks/04_classification_biologique_pipeline.ipynb) |
| 05 Validation et optimisation | validation croisée, recherche d'hyperparamètres, test final | [ouvrir](https://colab.research.google.com/github/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics/blob/main/notebooks/05_validation_et_optimisation.ipynb) |
| 06 Deep learning TensorFlow | neurone, gradient, réseau Keras, surapprentissage | [ouvrir](https://colab.research.google.com/github/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics/blob/main/notebooks/06_deep_learning_tensorflow.ipynb) |
| 07 Projet intégrateur | expression génique de leucémies, sélection sans fuite | [ouvrir](https://colab.research.google.com/github/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics/blob/main/notebooks/07_projet_integrateur_bioinformatique.ipynb) |

L'ebook `ebook/ebook_machine_learning_biologie.pdf` est le texte de référence qui accompagne les notebooks.

## Exécution

1. Dans Colab : ouvrir un notebook, puis *Exécution* puis *Tout exécuter*. Les notebooks 01 à 07 s'exécutent dans l'ordre et chacun est autonome.
2. En local :
   ```bash
   git clone https://github.com/DEDJIABDOUL/omicaa-lab-machine-learning-bioinformatics.git
   cd omicaa-lab-machine-learning-bioinformatics
   python -m venv .venv && source .venv/bin/activate
   pip install -r requirements.txt
   cd notebooks && jupyter lab
   ```
3. Le notebook 07 télécharge un fichier de 1,2 Mo : une connexion Internet est requise.
4. Temps d'exécution indicatifs sur un CPU : notebooks 01 à 05 et 07 en quelques minutes au total, notebook 06 environ 5 minutes.

Les notebooks écrivent dans leur dossier de travail `figures/`, `results/` (journaux JSON des résultats) et `models/`. Ces dossiers sont ignorés par Git.

## Sources des données

Voir [`data/README.md`](data/README.md). Breast Cancer Wisconsin (Diagnostic) : UCI, DOI 10.24432/C5DW2B, CC BY 4.0. Golub et al. (1999) : copie publique sur GitHub, **licence non vérifiée**.

## Bibliothèques

NumPy, pandas, Matplotlib, SciPy, scikit-learn, TensorFlow/Keras, joblib, rdata. Voir `requirements.txt` pour les versions de validation.

## Structure du dépôt

```
omicaa-lab-machine-learning-bioinformatics/
  README.md
  requirements.txt
  ebook/ebook_machine_learning_biologie.pdf
  notebooks/01 ... 07 (.ipynb)
  data/README.md
  references/README.md
```

## Reproductibilité

Graine aléatoire 42 partout. Les résultats chiffrés de l'ebook proviennent de l'exécution réelle des notebooks (Python 3.12, scikit-learn 1.8, TensorFlow 2.21). Les valeurs peuvent légèrement varier selon les versions et le processeur, en particulier pour TensorFlow.

## Limites scientifiques

* Les performances sont des estimations internes sur de petits jeux de données, avec une incertitude importante. Elles ne constituent pas une validation clinique.
* La copie du jeu Wisconsin ne permet pas de vérifier l'indépendance des observations.
* Le jeu de Golub compte 72 échantillons, dont 18 en test ; sa source est un miroir dont la licence n'est pas vérifiée.
* Un modèle prédictif exploite des associations statistiques et ne démontre aucun mécanisme biologique.
* Le deep learning est présenté à des fins pédagogiques ; il n'apporte pas de gain sur ces données tabulaires.

## Licence

À définir par l'auteur avant publication (code, contenu pédagogique). Les jeux de données conservent leurs licences respectives.
