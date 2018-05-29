# Exercise 1
[voir le site]()

## Objectifs

- Rajouter l'attribut `Alt` aux images. A quoi sert cet attribut?  
- Ajoute une classe "*bien*" ou "*mal*" aux balises entourant les mots "Bien" et "Mal".
- Trouve l'attribut des liens permettant d'indiquer la page vers laquelle doit mener le lien, et ajoute-le.  
- Fais en sorte que lorsqu'on clique sur les liens, la page s'ouvre dans un nouvel onglet du navigateur.  
- Trouve l'attribut permettant d'afficher une petite boite de texte au survol des liens, comme ceci :   
![Exemple](https://cdn.searchenginejournal.com/wp-content/uploads/2008/09/title-usability.jpg)
	
## 2. Le CSS : contrôler le rendu visuel

Le CSS est la techno qui te permet de contrôler l'aspect visuel de ton contenu.  Par exemple, tu peux contrôler l'aspect du texte via ces propriétés : `font-style`, `font-size`, `color`, `line-height`.

Autrement dit, si le html te permet de structurer le contenu, le CSS te permet de le **maquiller**, le rendre plus visuellement attractif.

### Syntaxe

```css
selecteur {
	propriete : valeur ;
	propriete : valeur ;
	/* Ceci est un commentaire */
	propriete : valeur ;
	...
}  
```

**Observations :**

- Chaque ligne doit se terminer par un `;`
- Tu peux déclarer autant de propriétés que tu le souhaites. Tu peux même déclarer deux fois la même propriété. Dans ce cas, ce sera la dernière qui sera prise en compte (d'où le terme "*cascading*").
- l'élément stylisé s'appelle "le sélecteur". Il est suivi d'un bloc contenant une ou plusieurs propriétés, enfermées dans des accolades `{}`

**Exemple** : à ton avis, que fait ce bout de code ? 

```css
p{
	font-size: 12px;
	font-family: Arial, sans-serif;
	color: purple;
}
```

Pour que le navigateur le prenne en compte, ton CSS doit se trouver soit :

- dans ton fichier html, dans une balise `<style>`
- dans un fichier css externe, lié à ton html via la balise `<link>`


### Concept 1: sélecteurs CSS

Les sélecteurs CSS te permettent de sélectionner dans ton html le contenu à styliser via la balise le contenant.


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
