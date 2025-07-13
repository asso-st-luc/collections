# Recommandations pour la Taille des Images

L'objectif est de trouver le meilleur équilibre entre la **qualité visuelle** et la **performance** (vitesse de chargement).

## Règle Générale : Le Double de la Taille d'Affichage

Pour garantir une netteté optimale sur les écrans modernes à haute densité (Retina, 4K), la largeur de votre image doit être environ **1.5x à 2x plus grande** que la taille maximale à laquelle elle sera affichée sur le site.

## Tailles Recommandées pour ce Projet

Ces tailles sont basées sur la largeur maximale du conteneur de contenu, qui est fixée à `720px` dans le CSS.

| Type d'image | Largeur d'affichage max. | **Largeur d'image recommandée** |
| :--- | :--- | :--- |
| **Image pleine largeur** (dans le corps du texte) | 720px | **~1400px - 1500px** |
| **Image flottante** (à gauche ou à droite du texte) | 360px (50% de 720px) | **~700px - 800px** |

## Processus d'Optimisation

1.  **Redimensionner :** Avant de téléverser l'image, redimensionnez-la aux largeurs recommandées ci-dessus avec un logiciel d'édition d'image.
2.  **Compresser :** C'est l'étape la plus importante pour réduire le temps de chargement.
    *   **Format :** Utilisez **WebP** si possible. Sinon, **JPEG** est un excellent choix pour les photographies.
    *   **Outils :** Utilisez des compresseurs en ligne comme [TinyPNG](https://tinypng.com/) / [TinyJPG](https://tinyjpg.com/) ou des logiciels dédiés pour réduire la taille du fichier sans perte de qualité visible.

## Pour Aller Plus Loin : `srcset` avec Hugo

Il est possible d'automatiser la création de plusieurs tailles d'images directement avec Hugo. En utilisant un `srcset`, le navigateur du visiteur télécharge automatiquement la taille d'image la plus adaptée à son écran, optimisant ainsi la performance au maximum. C'est une amélioration future possible.

---

## Annexe : Utiliser le Nombre d'Or (Ratio ≈ 1.618) pour des Proportions Harmonieuses

Le Nombre d'Or peut être utilisé pour définir la hauteur de vos images afin de créer un ratio esthétiquement plaisant.

Pour une image de **1400px de large** :

*   **Format Paysage (Recommandé) :**
    *   *Calcul :* `1400 / 1.618 ≈ 865`
    *   *Résolution :* **1400 x 865 pixels**

*   **Format Portrait :**
    *   *Calcul :* `1400 * 1.618 ≈ 2265`
    *   *Résolution :* **1400 x 2265 pixels**

**Conseil pratique :** Le format paysage est généralement plus adapté au web. Cependant, le plus important reste le cadrage du sujet de l'image. Utilisez le Nombre d'Or comme un guide, pas comme une règle absolue.

 ##The GIMP cecadrage 
 **Recadrer à une taille précise (1400x865)**
Ouvre ton image dans GIMP.

**Choisis l'outil de découpage :**
Menu Outils > Outils de transformation > Découpage
ou clique sur l’icône de découpage dans la boîte à outils (raccourci clavier : Maj + C).

Dans les options de l’outil (en bas de la boîte à outils) :

Coche Fixé : Taille.

Entres-y 1400 x 865 (assure-toi que l’unité est en pixels).

Clique sur l’image : un cadre de découpe apparaît.

Déplace le cadre à l’endroit souhaité (tu peux aussi le centrer ou le positionner manuellement).

Clique à l’intérieur du cadre ou appuie sur Entrée pour recadrer l’image.