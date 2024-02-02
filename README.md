# Booki Travel - Créez la page d'accueil d'une agence de voyage avec HTML & CSS
![Banner booki Travel](assets/images/Banner-Booki-Travel.png)

## Description

Ce projet a pour but de vous faire utiliser le langage HTML combiné au CSS.
Vous devez développer un site Internet qui permette aux usagers de trouver des hébergements et des activités dans la ville de leur choix.

## Table des matières

1. [Instructions](#instructions)
2. [Guide des étapes](#guide-des-étapes)<br>
2.1. [Étape 1 : Créez le repository](#étape-1--créez-le-repository)<br>
2.2. [Étape 2 : Créez la structure du projet](#étape-2--créez-la-structure-du-projet)<br>
2.3. [Étape 3 : Créez la branche develop](#étape-3--créez-la-branche-develop)<br>
2.4. [Étape 4 : Créez les issues](#étape-4--créez-les-issues)<br>
2.5. [Étape 5 : Créez la structure HTML du fichier ``index.html``](#étape-5--créez-la-structure-html-du-fichier-indexhtml)<br>
2.6. [Étape 6 : Remontez vos modifications à votre repository distant](#étape-6--remontez-vos-modifications-à-votre-repository-distant)<br>
2.7. [Étape 7 : Découpez votre maquette](#étape-7--découpez-votre-maquette)<br>
2.8. [Étape 8 : Intégrez le header du projet](#étape-8--intégrez-le-header-du-projet)<br>
2.9. [Étape 9 : Ajoutez le formulaire de recherche](#étape-9--ajoutez-le-formulaire-de-recherche)<br>
2.10. [Étape 10 : Ajoutez la zone des filtres](#étape-10--ajoutez-la-zone-des-filtres)<br>
2.11. [Étape 11 : Réalisez la section `Hébergement à Marseille` et `Les plus populaires`](#étape-11--réalisez-la-section-hébergement-à-marseille-et-les-plus-populaires)<br>
2.12. [Étape 12 : Intégrez le conteneur `Activités à Marseille`](#étape-12--intégrez-le-conteneur-activités-à-marseille)<br>
2.13. [Étape 13 : Implémentez le footer](#étape-13--implémentez-le-footer)<br>
2.14. [Étape 14 : Mettez en place le responsive design](#étape-14--mettez-en-place-le-responsive-design)<br>
2.15. [Étape 15 : Vérifiez la qualité de votre code](#étape-15--vérifiez-la-qualité-de-votre-code)

## Instructions

### Note Technique

Voici l’ensemble des points fonctionnels et techniques à prendre en compte pour le développement du nouveau
site Booki. L’ensemble de ces éléments a été validé par l’équipe Produit, il est donc important de les respecter.

**Spécifications fonctionnelles**
| **Fonction**              | **Description**           |
|-----------------------|-----------------------|
| Fonction recherche    | ● Les usagers pourront rechercher des hébergements dans la ville de leur choix<br>● Le champ de recherche est un champ de saisie, le texte doit donc pouvoir être édité par l’utilisateur.<br>● Il faut englober ce champ dans un formulaire. La partie Recherche ne doit pas être fonctionnelle - il s’agit d’une première version pour valider l’interface. |
| Liens Hébergements et Activités | ● Les textes ``Hébergements`` et ``Activités``, situés dans l’en-tête, sont des liens. Ils doivent mener respectivement vers la section ``Hébergements à Marseille`` et ``Activités à Marseille``. |
| Cartes hébergements et activités | ● Chaque carte d’hébergement ou d’activité devra être cliquable dans son intégralité (pas uniquement le titre).<br>● Pour l’instant, les liens sont vides. On peut utiliser un attribut `href="#"` pour simuler la présence d’un lien. |
| Filtres de recherche  | ● Les hébergements peuvent être filtrés par thématique, comme le budget ou l’ambiance.<br>● Les filtres doivent changer de couleur au survol de la souris.<br>● Les filtres ne doivent pas être fonctionnels - il s’agit juste d’une première version pour valider l’interface.. |

**Spécifications techniques**
| **Thème**                 | **Informations techniques**       |
|-----------------------|-------------------------------|
| Maquettes             | **Trois maquettes**  ont été réalisées : **desktop**, **tablette** et **mobile**. |
| Breakpoints           | Nous avons convenu avec le designer UI d’utiliser **1024px** et **768px** :<br>● >1024px pour les écrans d’ordinateurs ;<br>● >= 768px pour les tablettes ;<br>● et tout ce qui est en dessous de 768px pour les téléphones portables. |
| Largeur min - max     | ● Pour éviter d’étirer la page web sur la largeur de façon excessive, il va falloir déterminer une **largeur maximum de 1440px**. Au-delà, une marge blanche doit apparaître sur les côtés et le contenu doit se limiter à 1440px de large.<br>● Une **largeur minimum** doit être fixée à **320px**. En-deçà de cette largeur le comportement n'est pas garanti. |
| Desktop first         | Il faut d’abord réaliser l’intégration pour les ordinateurs (autrement dit, en desktop first), puis les tablettes et enfin les téléphones. L’utilisation des **Media Queries** vous permettra de réaliser l’intégration pour les différents supports. |
| Bibliothèque d’icônes | ● Les icônes proviennent de la bibliothèque [Font Awesome](https://fontawesome.com/docs/web/setup/get-started)    |
| Couleurs              | ● Les couleurs de la charte sont le **bleu (#0065FC)**, le **bleu clair (#DEEBFF)** et le **gris pour le fond (#F2F2F2)**. |
| Police                | ● La **police** du site est **Raleway**. Nous pouvons passer par **Google Fonts** pour importer facilement cette police dans le code : https://fonts.google.com/specimen/Raleway. |
| Mise en page          | ● Il est recommandé d'utiliser Flexbox. |
| Balises sémantiques   | ● Il est important d’utiliser des balises sémantiques, au minimum **header**, **nav**, **h1-h2-h3**, **main**, **section**, **article** et **footer**. |
| Validité du code      | ● Le **code** doit être valide aux **validateurs W3C** [HTML](https://validator.w3.org/) et [CSS](https://jigsaw.w3.org/css-validator/).<br>● Le code HTML ne doit pas contenir de propriété CSS.<br>● Privilégier l’utilisation des classes CSS pour cibler un élément, plutôt que d’utiliser le nom de l’élément lui-même.<br>● Ne pas dupliquer des classes CSS inutilement. Exemple : si 4 éléments sont identiques du point de vue de la mise en forme, alors utiliser une seule et même classe CSS, et non pas 4. |
| Compatibilité navigateurs | ● La **maquette** doit être **compatible** avec les dernières versions de **Google Chrome** et de **Mozilla Firefox**. Il faudra tester la page web sur ces deux navigateurs. |
| **Restrictions**     | ● **Aucun framework CSS** (type BootStrap ou Tailwind CSS) ou préprocesseur CSS (type Sass ou Less) ne doit être utilisé.<br>● **Aucun autre langage** ne doit être utilisé (comme JavaScript, par exemple). |

**Maquette**

[Maquette](https://www.figma.com/file/VtoblikCtKrTIVjT2ZBeAM/Maquettes-Booki---desktop%2C-mobile%2C-tablette?type=design&node-id=3%3A0&mode=design&t=TKtABOcWcnFEnV54-1)

## Guide des étapes

**Recommandations générales**
Dans ce projet, vous utiliserez **Figma** pour accéder aux maquettes desktop, tablette et mobile du site. Créez-vous un compte et connectez-vous à Figma afin d’avoir accès aux détails des éléments dans le menu de droite.

**Attention cependant :** vous pourrez accéder au code CSS de chaque élément. Vous pouvez repartir de ce code pour votre intégration si vous le souhaitez, mais il sera incomplet et nécessitera des modifications. Notamment, les dimensions sont toutes en pixels, mais vous aurez besoin d’en adapter certaines dans des valeurs relatives (unités `em` notamment).

### Étape 1 : Créez le repository
[![Progress](https://img.shields.io/badge/Progression-5%25-blue.svg)]()

**Une fois cette étape terminée, je dois avoir :**
- le projet créé sur un repo GitHub.

**Recommandations :**
1. Créez le repository sur GitHub ou le projet sur GitLab avec le nom **booki-travel**
2. Clonez le repository ou le projet sur votre ordinateur

**Ressources :**
- Le cours « `Gérez du code avec Git et GitHub` » ;

### Étape 2 : Créez la structure du projet 
[![Progress](https://img.shields.io/badge/Progression-10%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- mis en place le repo sur GitHub.

**Une fois cette étape terminée, je dois avoir :**
- créé l'architecture de mon projet.

**Recommandations :**
1. Créez le dossier **booki-travel**
2. Dans le dossier **booki-travel**, créez le dossier **assets** et le fichier **index.html**
3. Dans le dossier **assets**, créez les dossiers **css** et **images** 
4. Dans le dossier **css**, créez le fichier **style.css**
5. Dans le dossier **images** télécharger les images du dossier image du github
6. Réalisez un ``commit`` puis un ``push``. Pour réaliser un push sur GitLab il faut utiliser la commande `git push --set-upstream origin main`.

### Étape 3 : Créez la branche ``develop``
[![Progress](https://img.shields.io/badge/Progression-15%25-blue.svg)]()

Vous allez réaliser du versonning à partir de la branche ``develop``. A partir de cette branche vous allez créer des issues en lien avec les étapes / actions ci-dessous que vous devrez merger dans un premier temps sur la branche develop puis sur la branche principale main ou master.

**Avant de démarrer cette étape, je dois avoir :**
- l'architecture de mon projet.

**Une fois cette étape terminée, je dois avoir :**
- la branche develop de créée.

**Recommandations :**
1. Créez la branche ``develop`` au travers de votre terminal. Soit directement dans le terminal de votre IDE ou dans le terminal de votre ordinateur ou avec git bash.
2. Basculez sur la branche ``develop``

### Étape 4 : Créez les issues
[![Progress](https://img.shields.io/badge/Progression-20%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- créé la branche develop.

**Une fois cette étape terminée, je dois avoir :**
- tous les issues de créés.

**Recommandations :**
1. Créez les issues en lien avec les étapes 5, et 7 à 15 
- Mettez dans le champ **title** l'intitulé de l'étape
- Sélectionnez **issue** dans le champ **type**
- Mettez dans **description** le contenu de l'étape

### Étape 5 : Créez la structure HTML du fichier ``index.html``
[![Progress](https://img.shields.io/badge/Progression-25%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- tous les issues de créés.

**Une fois cette étape terminée, je dois avoir :**
- la structure HTML du fichier index.html.
- mon kit Font Awesome est créé et est appelé dans le fichier index.html
- l'appel à la font `Raleway`

**Recommandations :**
1. Ouvrez le dossier **booki-travel** dans votre IDE favoris (exemple VS Code)
2. Ouvrez le fichier **index.html** et insérez la structure de base HTML5
3. Indiquez la langue **fr** dans l'attribut ``lang`` de la balise ``html``
4. Dans la balise `head`, liez la feuille de style au fichier **index.html** et importez la police `Raleway` depuis Google Fonts ainsi que Font Awesome (avec la création de votre kit). Vous pouvez télécharger la font dans un dosseir fonts dans les assets. Pour cela il faudra utiliser `@font-face` dans la feuille de style

**Ressources :**
- [Documentation pour la création d'un kit Font Awesome](https://fontawesome.com/docs/web/setup/get-started)

## Étape 6 : Remontez vos modifications à votre repository distant
[![Progress](https://img.shields.io/badge/Progression-30%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- la structure HTML du fichier index.html.
- mon kit Font Awesome est créé et est appelé dans le fichier index.html
- l'appel à la font `Raleway`

**Une fois cette étape terminée, je dois avoir :**
- mon projet mis à jour sur GitHub.

**Recommandations :**
Dans cette étape, vous allez lier l'issue aux modifications que vous remontez à votre repository distant.
1. Enregistrez les modifications via la commande `git add .`
2. Réalisez un ``commit`` avec la commande `git commit -m "Création de la structure HTML du fichier index.html #1"`. Ici **#1** correspond au numéro de l'issue qu'il faut solder.
3. Réalisez un ``push``
4. Basculez sur la branche ``main`` puis réalisez un ``merge`` de la branche ``develop``
5. Rendez-vous sur votre repository et exécutez une ``pull request`` pour **GitHub** et une ``new merge request`` pour **GitLab**
6. Cloturez l'issue depuis votre repository

### Étape 7 : Découpez votre maquette
[![Progress](https://img.shields.io/badge/Progression-35%25-blue.svg)]()

Il est très important de découper la maquette avant de démarrer à coder.
Cela va vous permettre de visualiser les balises que vous allez utiliser dans votre code et ainsi bien structurer votre code.

**Avant de démarrer cette étape, je dois avoir :**
- mon projet mis à jour sur GitHub.

**Une fois cette étape terminée, je dois avoir :**
- une maquette découpée, représentant la structure du code HTML.

**Recommandations :**
1. Reprennez la maquette et découpez là par zone
2. Attribuez à chaque zone une balise et le plus possible une balise sémantique
3. Définissez à quel moment positionner les éléments de façon horizontale, ou bien de façon verticale. En effet, chaque bloc ne contient que des éléments positionnés soit horizontalement (par exemple, les filtres de la barre de navigation), soit verticalement (par exemple les cartes de la section « les plus populaires »).
4. Posez-vous les questions suivantes :
- Avez-vous pu identifier tout ce qui est visible sur la maquette (les éléments comme le logo, la fonction recherche, les cartes hébergements et activités etc.) ?
- Comment sont regroupés les différents éléments ?
- Pour chaque élément, quelle est la balise HTML qui lui est associée ?

**Points de vigilance :**
Ne perdez pas trop de temps à réaliser un découpage parfait. Le principal est d'avoir une vision rapide des principaux enjeux de la maquette.

### Étape 8 : Intégrez le header du projet
[![Progress](https://img.shields.io/badge/Progression-40%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- réalisé le découpage de la maquette.

**Une fois cette étape terminée, je dois avoir :**
- le code de l’en-tête de la page.

**Recommandations :**
1. Intégrer le header comme attendu par la maquette.
2. Remontez vos modifications à votre repository distant. Reprenez ici ce que vous avez réalisé à l'[Étape 6](#étape-6--remontez-vos-modifications-à-votre-repository-distant)

**Points de vigilance :**
- Attention à ne pas oublier la bordure bleue qui s’affiche au survol.
- Distinguez les moments où il faut utiliser une propriété margin plutôt que padding.
- Il est préférable d’utiliser des pixels plutôt que des pourcentages pour les valeurs des marges et des paddings.
- Les balises HTML ont des propriétés CSS par défaut (par exemple, un titre ``h1`` est affiché en gras par défaut).
- Il faut savoir que par défaut, la balise ``body`` comporte des marges.

**Ressources :**
- Appuyez-vous sur le `chapitre : Faites votre mise en page avec Flexbox` du cours `Créez votre site web avec HTML5 et CSS3`

### Étape 9 : Ajoutez le formulaire de recherche
[![Progress](https://img.shields.io/badge/Progression-45%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- intégré le header de la page.

**Une fois cette étape terminée, je devrais avoir :**
- un formulaire de recherche intégré à la page HTML.

**Recommandations :**
1. Intégrer le le formulaire de recherche en identifiant bien la construction de ce formulaire qui est constitué de 3 parties, comme on le voit sur la maquette.
2. Pour le moment, concentrez-vous sur la partie desktop, l’intégration de la partie responsive pourra se faire plus tard.
3. Ensuite, avec du CSS, il faudra afficher ou masquer le mot ou l’icône en fonction de l’écran utilisé.
4. Remontez vos modifications à votre repository distant. Reprenez ici ce que vous avez réalisé à l'[Étape 6](#étape-6--remontez-vos-modifications-à-votre-repository-distant)

**Points de vigilance :**
- Attention à ne pas appliquer une bordure sur l’intégralité du champ de recherche, pour que le visuel corresponde à la maquette.
- Attention au style de la barre de recherche : sur desktop, le bouton de recherche comprend le texte « Rechercher », alors que sur mobile, c’est une loupe. Pour gérer cela, il va falloir intégrer les deux éléments (le mot + l’icône) en HTML.

**Ressources :**
- Appuyez-vous sur le `chapitre : Créez des formulaires` du cours `Créez votre site web avec HTML5 et CSS3`

### Étape 10 : Ajoutez la zone des filtres
[![Progress](https://img.shields.io/badge/Progression-50%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- intégré le formulaire de recherche de la page.

**Une fois cette étape terminée, je devrais avoir :**
- la partie Filtre entièrement réalisée.

**Recommandations :**
1. Avec un bon découpage de la maquette, vous devriez pouvoir intégrer cette partie correctement avec Flexbox.
2. Commencez par intégrer les filtres sans vous préoccuper du changement d’apparence au survol.
3. Une fois les filtres en place, vous pouvez implémenter le changement de couleur de fond lors du survol.
4. Remontez vos modifications à votre repository distant. Reprenez ici ce que vous avez réalisé à l'[Étape 6](#étape-6--remontez-vos-modifications-à-votre-repository-distant)

**Points de vigilance :**
- Distinguez les moments où il faut utiliser une propriété margin plutôt que padding.
- Il est préférable d’utiliser des pixels plutôt que des pourcentages pour les valeurs des marges et des paddings. En effet, l'utilisation de pourcentages sur des marges/paddings ne correspondrait pas au résultat attendu, car les variations de taille risqueraient d’être trop fortes d'un format d'écran à un autre.

**Ressources :**
- Appuyez-vous sur le `chapitre : Découvrez le modèle des boîtes` du cours `Créez votre site web avec HTML5 et CSS3`

### Étape 11 : Réalisez les sections `Hébergement à Marseille` et `Les plus populaires`
[![Progress](https://img.shields.io/badge/Progression-60%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- intégré les filtres de la page.

**Une fois cette étape terminée, je devrais avoir :**
- les deux sections « *Hébergements à Marseille* » et « *Les plus populaires* ».

**Recommandations :**
1. Les cartes “*hébergements*” sont similaires aux cartes “*les plus populaires*”. Attention cependant, elles sont différentes, notamment dans le sens d’alignement des éléments : à l’horizontale pour “les plus populaires” et à la verticale pour les cartes “*hébergements*”.
2. Si aucune propriété CSS n’est appliquée sur une image, celle-ci va s’afficher dans sa taille d’origine. Comme pour de très nombreux éléments, donner une largeur en % à l’image est une bonne idée. Il sera nécessaire de définir une hauteur en pixels.
3. Une fois dimensionnée, l’image devrait être déformée. La propriété CSS `object-fit` permettra de corriger cela.
4. Remontez vos modifications à votre repository distant. Reprenez ici ce que vous avez réalisé à l'[Étape 6](#étape-6--remontez-vos-modifications-à-votre-repository-distant)

**Points de vigilance :**
- Les images doivent être intégrées via le HTML ;
- L'attributs alt des images doivent être renseignés ;
- Les cards ont une ombre portée ;
- Les cards ont un border-radius.

**Ressources :**
- L’article [How to – Cards de W3C](https://www.w3schools.com/howto/howto_css_cards.asp) avec quelques snippets de code pour réaliser une card ;
- L’article [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/object-fit) sur la propriété « object-fit ».
- Appuyez-vous sur le `chapitre : Faites votre mise en page avec Flexbox` du cours `Créez votre site web avec HTML5 et CSS3`

### Étape 12 : Intégrez le conteneur `Activités à Marseille`
[![Progress](https://img.shields.io/badge/Progression-70%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- intégré les deux sections « *Hébergements à Marseille* » et « *Les plus populaires* » de la page.

**Une fois cette étape terminée, je devrais avoir :**
- le projet presque terminé. Il ne restera plus que le footer à réaliser.

**Recommandations :**
1. Appuyez-vous sur les précédentes recommandations données pour la réalisation des différentes cartes.
2. Dans cette section, la structure est un peu différente puisque c’est une présentation en 4 colonnes.
3. La hauteur de chacune des activités est identique. Il faudra alors mettre en place (comme dans les étapes précédentes) une première activité, et
intégrer les 3 autres à partir de la première.
4. Remontez vos modifications à votre repository distant. Reprenez ici ce que vous avez réalisé à l'[Étape 6](#étape-6--remontez-vos-modifications-à-votre-repository-distant)

**Points de vigilance :**
- Les images doivent être intégrées via le HTML ;
- L'attributs alt des images doivent être renseignés ;
- Les cards ont une ombre portée ;
- Les cards ont un border-radius.

**Ressources :**
- L’article [How to – Cards de W3C](https://www.w3schools.com/howto/howto_css_cards.asp) avec quelques snippets de code pour réaliser une card ;
- L’article [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/object-fit) sur la propriété « object-fit ».
- Appuyez-vous sur le `chapitre : Faites votre mise en page avec Flexbox` du cours `Créez votre site web avec HTML5 et CSS3`

### Étape 13 : Implémentez le footer
[![Progress](https://img.shields.io/badge/Progression-80%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- intégré la section « *Activités à Marseille* » de la page.

**Une fois cette étape terminée, je devrais avoir :**
- terminé le code du projet.

**Recommandations :**
1. Une fois encore, vous pouvez utiliser Flexbox pour la mise en page.
2. Il faudra bien vous appuyer sur le découpage de votre maquette, et identifier les différents éléments ainsi que les différents blocs.
3. Le footer se présente sous 3 colonnes de tailles identiques.
4. Remontez vos modifications à votre repository distant. Reprenez ici ce que vous avez réalisé à l'[Étape 6](#étape-6--remontez-vos-modifications-à-votre-repository-distant)

**Points de vigilance :**
- Si vous utilisez des `ul` pour réaliser les liens, vous avez par défaut un `padding-left` qui s’applique. Pensez à l’enlever, car cela va provoquer un décalage par rapport à ce qui se trouve juste au-dessus.

**Ressources :**
- Appuyez-vous sur le `chapitre : Faites votre mise en page avec Flexbox` du cours `Créez votre site web avec HTML5 et CSS3`

### Étape 14 : Mettez en place le responsive design
[![Progress](https://img.shields.io/badge/Progression-90%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- La version desktop du site, pleinement fonctionnelle, se comportant
correctement de la résolution 1024px à la résolution 1440px.

**Une fois cette étape terminée, je devrais avoir :**
- Un projet pleinement compatible avec toutes les tailles d’écran possibles.

**Recommandations :**
1. Respectez bien les deux media queries définies : <=1024px pour l’affichage tablette et <768px pour l’affichage mobile ;
3. Pensez bien à respecter l’ordre du code dans le CSS : d’abord le code CSS global, puis la media query tablette, puis la version mobile.
4. Pensez à définir une largeur maximum à 1440px pour gérer correctement les écrans avec une grande résolution, ainsi qu’une largeur minimum de 320px.
5. Remontez vos modifications à votre repository distant. Reprenez ici ce que vous avez réalisé à l'[Étape 6](#étape-6--remontez-vos-modifications-à-votre-repository-distant)

**Points de vigilance :**
- Pensez à conserver la meta viewport fournie dans le code HTML.
- Les couleurs de fond de certaines sections s'inversent entre la version mobile et la version desktop

**Ressources :**
- Le chapitre `Utilisez le responsive design avec les Media Queries` du cours `Créez votre site web avec HTML5 et CSS3` ;
- L’article [Utilisation de la balise meta viewport pour contrôler la mise en page sur mobile](https://developer.mozilla.org/fr/docs/Web/HTML/Viewport_meta_tag).

### Étape 15 : Vérifiez la qualité de votre code
[![Progress](https://img.shields.io/badge/Progression-100%25-blue.svg)]()

**Avant de démarrer cette étape, je dois avoir :**
- Terminé d’intégrer les maquettes, sur tous les formats d’écran.

**Une fois cette étape terminée, je devrais avoir :**
- Terminé le projet !

**Recommandations :**
1. Concentrez vos efforts sur les erreurs remontées. Vous pouvez regarder les warnings, mais vous n’êtes pas obligé de les traiter.
2. Faites attention au nommage du code (des classes CSS, par exemple). Vous pouvez utiliser l’anglais ou le français, mais évitez de mixer les deux langues.
3. Utilisez le kebab case, par exemple `.main-wrapper` . C’est LA convention CSS la plus répandue.
4. Préférez généralement l’utilisation des pixels pour les margins/paddings, et les pourcentages pour les widths, dans le but de permettre la bonne gestion des différentes résolutions. Dans certains cas, l’utilisation de pixels pour les widths peut être quelque chose de pertinent (gestion de la taille d’une icône, par exemple).
5. Remontez vos modifications à votre repository distant. Reprenez ici ce que vous avez réalisé à l'[Étape 6](#étape-6--remontez-vos-modifications-à-votre-repository-distant)

**Ressources :**
- Les outils de validation de code : [Validateur HTML du W3C](https://validator.w3.org/) ;
