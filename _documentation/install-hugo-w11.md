# Installer Hugo sur Windows 11 avec Winget

Cette méthode utilise **Winget**, le gestionnaire de paquets officiel de Windows, intégré à Windows 11. C'est la méthode la plus simple et recommandée.

### Étape 1 : Ouvrir le Terminal en mode Administrateur

Faites un clic droit sur le menu Démarrer et sélectionnez **Terminal (administrateur)**.

![Ouvrir le terminal en mode admin](https://i.imgur.com/n0v4FqH.png)

### Étape 2 : Installer Hugo "Extended"

Il est fortement recommandé d'installer la version **"extended"** de Hugo, car de nombreux thèmes en dépendent pour fonctionner correctement.

Copiez et collez la commande suivante dans le terminal, puis appuyez sur `Entrée` :

```shell
winget install Hugo.Hugo.Extended
```

Winget va télécharger et installer Hugo pour vous. Acceptez les conditions si nécessaire.

### Étape 3 : Vérifier l'installation

Une fois l'installation terminée, **fermez et rouvrez** votre fenêtre de terminal. C'est une étape importante pour que le système reconnaisse la nouvelle commande.

Pour vérifier que Hugo est bien installé, tapez la commande suivante :

```shell
hugo version
```

Vous devriez voir un message s'afficher avec le numéro de version de Hugo, confirmant que l'installation a réussi. Par exemple :

```
hugo v0.125.5-b659501971e22241f232a7ade0635a7a012d36e4+extended windows/amd64 BuildDate=2024-04-26T16:25:09Z VendorInfo=gohugoio
```

C'est tout ! Hugo est maintenant prêt à être utilisé sur votre système.

---

## Résoudre les Problèmes d'Affichage des Caractères Accentés (Encodage)

Si vous rencontrez des problèmes d'affichage des caractères accentués (par exemple, avec `winget`), cela est souvent dû à un problème d'encodage du terminal. Voici la solution recommandée pour Windows 11.

### Solution Définitive : Activer l'UTF-8 Globalement

Cette option modifie un paramètre global de Windows pour que les applications utilisent UTF-8 par défaut, ce qui est la meilleure solution à long terme.

1.  **Ouvrir les Paramètres de Région :**
    *   Appuyez sur la touche `Windows`, tapez `International` et ouvrez **"Paramètres de langue"**.
    *   Cliquez sur **"Paramètres d'administration de la langue"**.

2.  **Modifier les Paramètres Régionaux du Système :**
    *   Dans la nouvelle fenêtre, sous l'onglet **"Administration"**, cliquez sur le bouton **"Modifier les paramètres régionaux du système..."**.

3.  **Activer l'option Bêta UTF-8 :**
    *   Cochez la case : **"Bêta : Utiliser Unicode UTF-8 pour la prise en charge des langues du monde entier"**.
    *   Cliquez sur **"OK"**.

4.  **Redémarrer l'ordinateur :**
    *   Windows vous demandera de redémarrer pour que le changement prenne effet. C'est indispensable.

Après le redémarrage, les caractères accentués devraient s'afficher correctement dans votre terminal et avec `winget`.