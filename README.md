# La collection de l'association Saint Luc Images

Ce dépôt contient le code source du site web "La collection de l'association Saint Luc Images", généré avec [Hugo](https://gohugo.io/) et utilisant le thème `nibble`.

Le site est déployé automatiquement sur GitHub Pages via GitHub Actions.

### Répertoire documentation 

Le répertoire _documentation contient des indications pour la taille des images.

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

 1. Public Cible : À qui s'adresse principalement le contenu (grand public, experts, jeunes, etc.) ? Cela influence
      le ton, le vocabulaire et le niveau de détail.
   2. Ton et Voix : Le ton doit-il être formel, informel, didactique, narratif, ou un mélange ? Y a-t-il une "voix"
      spécifique à adopter pour l'association ?
   3. Longueur des Articles : Y a-t-il une fourchette de mots souhaitée pour les articles (au-delà de la moyenne
      actuelle) ? Par exemple, un minimum ou un maximum.
   4. Gestion des Sources et Citations : Comment les sources (documents d'archives, livres, etc.) doivent-elles être
      citées ou référencées dans le texte ? (ex: notes de bas de page, bibliographie, liens hypertextes).
   5. Directives sur les Images :
       * Dimensions/Résolution : Y a-t-il des tailles ou résolutions d'image préférées/requises ?
       * Optimisation : Des exigences spécifiques en matière de compression ou de format de fichier pour le web ?
       * Licences/Droits d'auteur : Comment gérer les droits d'auteur des images ? Faut-il toujours mentionner la
         source ?
   6. Mots-clés/Thèmes : Y a-t-il une liste de mots-clés ou de thèmes principaux à privilégier pour le référencement
      ou la catégorisation du contenu ?
   7. Fréquence de Publication : Y a-t-il un calendrier ou une fréquence de publication prévue pour le nouveau
      contenu ?

      
✦ Pour que je puisse structurer vos notes en fichiers index.md avec leurs répertoires associés de manière efficace
  et conforme aux directives, voici la forme minimale que vos notes devraient prendre pour chaque section ou
  article :

  Chaque section de notes devrait être délimitée par --- au début et à la fin de son "front matter", suivi du
  contenu.



   1 ---
   2 Titre: [Titre de votre section/article]
   3 Poids: [Numéro pour l'ordre de la section, ex: 10, 20, 30...]
   4 Parent: [Nom du répertoire parent existant, ex: La-chapelle-saint-gregoire. Laissez vide si c'est une 
     nouvelle section de niveau supérieur.]
   5 ---
   6 [Contenu de votre section en Markdown. Vous pouvez utiliser des paragraphes, des listes, etc.]
   7 
   8 [Si vous avez une image associée à cette section, indiquez-la sur une nouvelle ligne comme ceci :]
   9 [IMAGE: nom_du_fichier_image.jpg, CAPTION: Légende descriptive de l'image.]



  Explication des champs :


   * `Titre:` : Le titre de votre section. Ce sera utilisé pour le champ title dans le "front matter" et pour créer
     le nom du répertoire (en version "slugifiée", c'est-à-dire sans espaces ni caractères spéciaux).
   * `Poids:` : Un nombre entier qui déterminera l'ordre de cette section par rapport aux autres dans le même
     répertoire parent. Assurez-vous que les poids sont uniques et logiques au sein d'un même niveau.
   * `Parent:` : (Optionnel) Si cette section est une sous-section d'une section existante (par exemple, une
     nouvelle étape dans "La-chapelle-saint-gregoire"), indiquez le nom du répertoire parent. Si vous ne spécifiez
     pas de Parent, je considérerai que c'est une nouvelle section de niveau supérieur sous content/.
   * Contenu : Le corps principal de votre texte, rédigé en Markdown.
   * `[IMAGE: nom_du_fichier_image.jpg, CAPTION: Légende descriptive de l'image.]` : (Optionnel) Si votre section
     doit inclure une image, fournissez le nom exact du fichier image et sa légende. Je générerai le shortcode Hugo
     {{< figure >}} approprié. Notez que vous devrez me fournir les fichiers images séparément.

  Exemple de notes que vous pourriez me donner :



    1 ---
    2 Titre: La Nouvelle Étape
    3 Poids: 70
    4 Parent: La-chapelle-saint-gregoire
    5 ---
    6 Après de nombreuses discussions, l'association a décidé de franchir une nouvelle étape dans son 
      développement. Cette phase se concentrera sur l'élargissement de notre portée.
    7 
    8 Nous prévoyons d'organiser des événements réguliers pour engager la communauté locale.
    9 
   10 [IMAGE: evenement_communaute.png, CAPTION: Un rassemblement communautaire.]
   11 
   12 ---
   13 Titre: Notre Vision Future
   14 Poids: 10
   15 Parent:
   16 ---
   17 Notre vision pour l'avenir est de devenir un pilier central pour la préservation du patrimoine local.
      Nous croyons fermement que la culture et l'histoire sont essentielles pour le bien-être de notre 
      société.
   18 
   19 Nous invitons tous les passionnés à nous rejoindre dans cette aventure.



  Avec ce format, je pourrai :
   1. Créer le répertoire content/[Parent]/[titre-slugifié]/ (ou content/[titre-slugifié]/ si Parent est vide).
   2. Créer le fichier index.md à l'intérieur.
   3. Remplir le "front matter" avec le title, weight, la date actuelle et draft = false.
   4. Insérer votre contenu Markdown.
   5. Convertir les balises [IMAGE: ...] en shortcodes {{< figure >}} de Hugo.
