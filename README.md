# Skin-Cancer-Detection


Ce projet met en œuvre un modèle CNN basé sur le mécanisme d’attention CBAM (Convolutional Block Attention Module) pour la classification de 9 types de lésions cutanées à partir d'images dermatoscopiques.

##  Dataset

- **Nom** : [Skin Cancer ISIC – 9 Classes](https://www.kaggle.com/datasets/nodoubttome/skin-cancer9-classesisic)
- **Source** : Kaggle – NoDoubtToMe (en lien avec l’ISIC)
- Les données sont organisées par dossier (1 par classe)

##  Prétraitement

- Augmentation via la bibliothèque `Augmentor`
- 6000 images par classe pour l'entraînement
- 1200 images par classe pour la validation
- Format : 128x128 RGB, JPG

##  Modèle utilisé

- CNN profond 6 blocs
- Bloc CBAM à chaque étape convolutive (attention spatiale + canal)
- Entraîné avec :
  - `Adam`
  - `EarlyStopping`
  - `ReduceLROnPlateau`
  - `ModelCheckpoint`

##  Résultats

- Accuracy validation finale : ** 98 %**
- Matrice de confusion, courbes d’apprentissage, etc. disponibles dans les annexes du mémoire.

##  Fichiers

- `main.ipynb` : notebook du modèle complet
- `augmentation_data.ipynb` : génération des données augmentées
- `requirements.txt` : dépendances pour l’exécution

## Par

- Yanis Habarek – Mastère Dev, Data & IA – IPSSI SQY
