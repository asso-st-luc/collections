## Directives Éditoriales pour le Contenu Hugo

Ces directives visent à assurer l'homogénéité et la qualité du contenu publié sur le site.

### Directives Générales

1.  **Format Markdown avec Front Matter (TOML):**
    *   Chaque fichier `index.md` doit commencer par un bloc de "Front Matter" au format TOML (délimité par `+++`).
    *   Les champs obligatoires sont : `title`, `date`, `weight`, et `draft`.
    *   `title`: Titre de la page/section.
    *   `date`: Date de création/dernière modification au format `YYYY-MM-DDTHH:MM:SS+ZZ:ZZ` (ex: `2024-08-28T10:39:21+02:00`).
    *   `weight`: Numéro pour ordonner les pages/sections dans une liste. Assurez-vous que les poids sont cohérents au sein d'une même section parent.
    *   `draft`: `true` si la page est en brouillon, `false` si elle est prête à être publiée.

2.  **Structure du Contenu:**
    *   Utilisez le balisage Markdown standard pour les titres (`#`, `##`, etc.), les paragraphes, les listes, etc.
    *   Utilisez `<!--more-->` pour définir le résumé de l'article qui apparaîtra sur les pages de liste. Le texte avant ce marqueur sera le résumé.

3.  **Cohérence Thématique:**
    *   Chaque section (dossier) doit avoir un thème clair et être développée de manière logique.
    *   Les titres des pages (`title` dans le Front Matter) doivent être concis et descriptifs.

### Directives Spécifiques au Contenu

1.  **Introduction et Contexte:**
    *   Pour les sections introductives (`00-intro`), fournissez un aperçu général du sujet et son contexte.
    *   Si des documents d'archives ou des sources sont utilisés, mentionnez leur nature et leur importance.

2.  **Narration et Style:**
    *   Le ton est informatif et explicatif.
    *   Utilisez un langage clair et accessible.
    *   Évitez le jargon technique excessif sans explication.
    *   Chaque page ajoute un élément narratif clair et utile pour la compréhension globale.


3.  **Utilisation des Images:**
    *   Utilisez le shortcode `figure` de Hugo pour insérer des images, comme ceci :
        ```html
        {{< figure src="/chemin/vers/image.jpg" caption="Légende de l'image." align="right" >}}
        ```
    *   `src`: Chemin relatif de l'image depuis le dossier `static` ou le dossier de la page courante.
    *   `caption`: Légende descriptive de l'image.
    *   `align`: `left`, `right`, ou `center` pour l'alignement.
    *   Assurez-vous que les images sont pertinentes et de bonne qualité.
    *   Nommez les fichiers d'images de manière descriptive et cohérente (ex: `01-le-tableau.jpg`).

4.  **Références et Précisions:**
    *   Si vous faites référence à des dates, des personnes ou des événements, assurez-vous de leur exactitude.
    *   Ajoutez des précisions historiques ou contextuelles si nécessaire pour la compréhension du lecteur.

5. **Taille du contenu**
    * chaque fichier index.md ne doit pas contenir plus de 70 mots.

### Recommandations Techniques

*   **Nommage des Fichiers et Dossiers:**
    *   Utilisez des noms de dossiers et de fichiers en minuscules, sans espaces, et avec des tirets (`-`) pour séparer les mots (ex: `la-chapelle-saint-gregoire`, `00-intro`).
    *   Les dossiers numérotés (ex: `00-intro`, `05-perplexite`) sont utilisés pour maintenir un ordre chronologique ou logique.

*   **Chemins des Images:**
    *   Les chemins des images dans le shortcode `figure` doivent être absolus depuis la racine du site (ex: `/Le-tableau-de-choeur/01-Le-Tableau/01-le-tableau.jpg`) ou relatifs à la page si l'image est dans le même dossier que l'index.md.
