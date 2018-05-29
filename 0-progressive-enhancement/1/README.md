# Exercise 1
[voir le site]()

## Objectifs

**Exercices :**  

- Retranscris [ce document Texte](doc-le-paysan-chinois.txt) en sémantique html, donc en utilisant les bons blocs html : Utilise les balises suivantes: `h1`, `h2`, `blockquote`, `q`, `img`, `p`, `img`, `hr`, `figure` et `caption`, `table`, `th`, `tr`, `td`, `ul` ou `ol` et `li`. 
- Pas de `div` ni de `span` : elles n'apportent aucune sémantique. 
- Retrouve, pour chacune de ces balises, l'origine de leur nom (c'est comme cela qu'on les retient). En cas de doute, cherche la réponse sur [html5doctor.com](http://html5doctor.com).
- Ajoute deux ou trois liens de ton choix dans la page html via la balise `a`
- Y-a-t-il une partie que l'on pourrait considérer comme une entête? Si oui, regroupe la dans une balise `header`. 
- Et un pied de page? Si oui, regroupe ce contenu là dans une balise `footer`
- Mets toutes les instances des mots "Bien" et "Mal" dans une balise `span` , `em` ou `strong`. 

- Rajouter l'attribut `Alt` aux images. A quoi sert cet attribut?  
- Ajoute une classe "*bien*" ou "*mal*" aux balises entourant les mots "Bien" et "Mal".
- Trouve l'attribut des liens permettant d'indiquer la page vers laquelle doit mener le lien, et ajoute-le.  
- Fais en sorte que lorsqu'on clique sur les liens, la page s'ouvre dans un nouvel onglet du navigateur.  
- Trouve l'attribut permettant d'afficher une petite boite de texte au survol des liens, comme ceci :   
![Exemple](https://cdn.searchenginejournal.com/wp-content/uploads/2008/09/title-usability.jpg)
	

**Exercices :**  

Reprends ton fichier du paysan chinois :

- stylise les paragraphes : utilise une police à empatement, augmente un peu l'interlignage, utilise une taille de base bien lisible. Donne au texte de couleur foncée, mais pas noire.
- stylise les liens de manière à les rendre bien lisibles.
- stylise l'état "survolé" et l'état "visité" des liens.

### Concept 2: le bloc
 
Toute balise est rendue visuellement sous forme de "bloc" (en anglais on parle du [box model](https://www.w3schools.com/css/css_boxmodel.asp)).  

![Le bloc](css-block.png)  

Tu peux contrôler les dimensions et les espacements de ce bloc :   

- `width`/ `height` : dimensions de largeur et hauteur 
- `border`: contrôle la bordure. Par exemple: `border:1px solid #FF0000;` crée un bord fait d'un trait continu (`solid`) rouge `#FF0000` et de 1px d'épaisseur
- `padding` : l'espace entre le contenu du bloc et son contour (le `border`). Le padding "gonfle" le bloc.  
- `margin` : l'espace autour du bloc, à l'extérieur de lui. Le margin distancie le bloc de son entourage.  


**Exercices :**  

Reprends ton fichier du paysan chinois :

- Donne au `body` une largeur maximum de 90% 
- Ensuite, centre le `body` en jouant avec la propriété `margin`  
- Fais en sorte que les citations ne prennent en largeur que la moitié de la page   
- En utilisant uniquement la propriété `margin`, positionne les citations au milieu.  
- Augmente la taille du texte dans les citations à 160% de la taille du texte par défaut  
- Donne une couleur légèrement grisée au fond des citations   
- Ajoute une bordure à gauche de chaque citation, de 3px et de couleur brique    
- Le texte des citations touche la bordure, ce n'est pas joli. Ajoute un espace de 30px entre la bordure et le texte de la citation.  
- Fais en sorte que les citations aient un espace vide de 80 pixels au dessus et en dessous.  
- Trouve comment ajouter une couleur de fond à ton `body`
- Change la couleur de fond pour utiliser un dégradé de couleur (va sur [http://www.colinkeany.com/blend/](http://www.colinkeany.com/blend/))
- ajoute une image de fond à ton `body`
- fais en sorte que l'image ne se répète pas 
- change son positionnement à `bottom right` 
- change sa taille à `cover`

### Les sélecteurs en CSS (part 2) : 
#### Les plus courants
Le plus souvent, on sélectionne les éléments à styliser via l'attribut `class` (`.nom-de-la-classe`) et `id` (`#nom-de-lid`).  

**Exercices**   

Reprends ton fichier du paysan chinois :

- En utilisant uniquement la balise comme sélecteur, mets toutes les citations en italiques.  
	- Identifie les citations des villageois et celles du fermier en assignant à chacune une classe correspondante.  
	- Change la couleur du bord gauche des citations en fonction de la personne qui parle.  

#### Sélectionner via parent et enfant  

**Exercice**

Reprends ton fichier du paysan chinois :

- Sélectionne un élément du `header` et donne lui un fond jaune.

#### Tous les autres sélecteurs
 
-  `+` et `>` 
-  	Sélectionner via l'attribut `[attribute]`
-   Il y en a quelques autres. Pour te faire une idée de ce qu'ils permettent, va lire la petite [doc officielle](https://www.w3schools.com/cssref/css_selectors.asp), puis joue à [CSS Diner](http://flukeout.github.io/)

**Exercices**  

Reprends ton fichier du paysan chinois :

-   Mets en italique le texte des citations
-   Mets en lettres majuscules toutes les instances des mots "bien" et "mal".
-   Mets en rouge les mots "Mal"
-   Mets en vert les mots "Bien"
-   Stylise la table pour que la couleur de fond de chaque rangée soit en alternance grise ou blanche
-   Au premier élément de la liste (les types de gens), joue avec `background-image` et `padding-right` pour faire apparaître l'image ![bien](bien.png)  
-   Au deuxième élément de la liste (les types de gens), joue avec `background-image` et `padding-right` pour faire apparaître l'image  ![mal](mal.png)  
-   Au troisième élément de la liste (les types de gens), joue avec `background-image` et `padding-right` pour faire apparaître l'image  ![chat](chat.png)  
-   Mets en gras le premier paragraphe

		
### Concept 3: le positionnement en CSS
Le CSS te permet de définir le positionnement visuel des éléments. C'est probablement le plus riche et donc le plus complexe, car les manières de contrôler le positionnement a eu une histoire plutôt compliquée. Il y a longtemps fallu utiliser des *hacks*. Les choses sont plus stables maintenant, surtout s'il ne faut pas supporter les utilisateurs coincés sur internet explorer 9...  Mais reprenons les choses à leur commencement.
 
#### Comprendre le flux

Chaque bloc html hérite (= "reçoit par défaut") d'une propriété "display" qui est soit : `display: inline | inline-block | block`  et s'affiche en fonction de son ordre d'apparition dans le fichier html. C'est ce que l'on appelle le **flux de positionnement naturel** ou plus simplement le **flux**.

-  Théorie interactive : https://codepen.io/pixeline/pen/QvrbPv 
-  Exercice : un menu horizontal https://codepen.io/pixeline/pen/PmdPYL 
-  Exercice : une grille https://codepen.io/pixeline/pen/aWavWq  
-  `float` va laisser le block flotter sur le block suivant (au lieu de le pousser à la ligne)

**Exercice :**  

Reprends ton fichier du paysan chinois :

- Fais en sorte que le texte courre autour des images, en utilisant, sur les images, la propriété `float` (ajuste avec du `margin` pour distancier le texte de l'image).
