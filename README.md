# La collection de l'association Saint Luc Images

Ce dépôt contient le code source du site web "La collection de l'association Saint Luc Images", généré avec [Hugo](https://gohugo.io/) et utilisant le thème `nibble`.

Le site est déployé automatiquement sur GitHub Pages via GitHub Actions.

## Démarrage rapide (Local)

Pour faire fonctionner ce projet en local, assurez-vous d'avoir [Hugo](https://gohugo.io/getting-started/installing/) installé.

1.  **Cloner le dépôt :**
    ```bash
    git clone https://github.com/asso-st-luc/collections-bootStrap.git
    cd collections-bootStrap
    ```

2.  **Initialiser les sous-modules (thème) :**
    ```bash
    git submodule update --init --recursive
    ```

3.  **Lancer le serveur de développement :**
    ```bash
    hugo server
    ```
    Le site sera accessible à l'adresse `http://localhost:1313/`.

## Structure du projet

-   `content/`: Contenu du site (articles, pages, etc.).
-   `static/`: Fichiers statiques (images, CSS, JS non traités par Hugo).
-   `themes/nibble/`: Le thème Hugo utilisé pour ce site.
-   `hugo.toml`: Fichier de configuration principal d'Hugo.
-   `.github/workflows/hugo.yaml`: Configuration du déploiement automatique sur GitHub Pages.

## Déploiement

Le déploiement est géré par GitHub Actions. Chaque push sur la branche `master` déclenche un workflow qui construit le site et le déploie sur GitHub Pages à l'adresse : `https://asso-st-luc.github.io/collections/`.

## Copyright

© Association Saint Luc Images
