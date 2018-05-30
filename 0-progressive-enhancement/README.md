# L'Amélioration progressive

- Repository à créer : `progressive-enhancement` 
- Slides : [Progressive Enhancement](https://app.ludus.one/8c042d9a-e404-4df5-b14e-48e3eb6e6014)
- Temps nécessaire : 3-4 jours.

## 1. HTML : la sémantique

Ca veut dire quoi "**sémantique**" ?  

Une phrase n'a pas la même signification si elle est mise en titre ou si elle est mise en pied de page, pas vrai ?  La sémantique, c'est cela : cela renvoie au sens, à la signification d'un contenu en observant sa structure. 

Par conséquent, pour bien composer un document html, il faut raisonner non pas en termes d'apparence graphique mais en termes de définition de chacun des objets le composant, c.à.d. **raisonner en terme de structure** :sparkling_heart:.  

**Comment ?** Faire du html sémantique consiste à se poser la question: "*Ce bout de texte, c'est quoi: un titre? Un paragraphe? Une légende? Et ce bloc, est-ce un chapitre ? Une note de l'auteur ?*" et en fonction de la réponse, choisir la balise correspondante ou s'en rapprochant le plus.

### Pourquoi la sémantique est importante pour ta carrière 

Pour deux raisons :  la **SEO** (position de ton site dans Google) et **l'Accessibilité** (accès à l'information pour tout humain, peu importe son âge ou d'éventuels handicaps).  

#### 1.1 SEO
L'objectif ultime d'un moteur de recherche comme Google est de retourner à un humain les meilleurs résultats possibles pour ce qu'il a cherché (quelques mots). Pour ce faire, Google crée des logiciels tels que le **Googlebot**, qui indexe le contenu trouvé sur le web en suivant les liens d'une page à une autre, d'un site à l'autre. (C'est pour cela qu'on parle parfois de *web spiders*).  

Via des algorithmes puissants, Google lit et analyse le contenu HTML de chaque page trouvée, afin de "comprendre" ce dont elle parle grâce à sa structure html (titre, sous-titre, liste, etc). Elle peut ainsi déterminer ce dont parle chaque page, et si celle-ci semble correspondre à la recherche, elle va la retourner à l'utilisateur.

**Par conséquent, si nos pages ne sont pas bien sémantiques, Google ne les montrera pas, et nos sites n'auront pas de traffic.**

Voici une jolie citation pour exprimer cela :  

> Findability Precedes Usability
> In the Alphabet and on the Web.
> You Can't Use What You Can't Find.
> – [Peter Morville](https://thatsthespir.it/quote/view/10)

#### 1.2 Accessibilité
Le web est un projet universel : tout le monde doit avoir accès au contenu. En ce compris les aveugles et mal voyants (toi, un jour). Les aveugles utilisent des "liseuses d'écran" (*screen readers*) qui se basent sur le code html pour raconter le site à voix haute. Si ton code html n'est pas sémantique, la page n'aura pas beaucoup de sens à l'écoute (même si visuellement elle rend correctement). N'hésite pas à [tester sur ton propre ordinateur](https://stackoverflow.com/a/43368748/53960).

### Concrètement, la sémantique, c'est simple.
 
La sémantique consiste à choisir les bonnes **balises** et **attributs** pour représenter ton contenu. Note bien que trop de sémantique tue la sémantique. La règle (comme souvent en programmation) est :  **le moins de code possible, mais autant que nécessaire.**

#### Balises
Les balises permettent d'indiquer la fonction sémantique d'une portion de contenu dans des "blocs". La plupart des blocs html fonctionnent avec une balise d'ouverture et une balise de fermeture.

**Exemple de syntaxe :**

```html
<p>Ceci est un paragraphe.</p>
```

#### Les attributs html
Ils permettent de définir les caractéristiques des balises.  Imagine qu'il y ait une balise "humain". 

```html
<p>
Steven Paul Jobs, dit Steve Jobs, (San Francisco, 24 février 1955 - Palo Alto, 5 octobre 2011) est un entrepreneur...
</p>
```   

Nous pouvons, avec des attributs, décrire cet humain pour le différencier des autres.

```html
<p type="human" name="Steve Job" nationality="USA" origin="Syria" job="CEO" company="Apple" hair="grey">
Steven Paul Jobs, dit Steve Jobs, (San Francisco, 24 février 1955 - Palo Alto, 5 octobre 2011) est un entrepreneur...
</p>
```  

De la sorte, en augmentant la sémantique des balises par des attributs, on a ainsi clarifié pour une machine qui est cet humain là. 

Voici résumée la syntaxe des balises, attributs et valeurs :

```html
<balise attribut="valeur">Contenu</balise> 
``` 

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

### Concept 2: le bloc
 
Toute balise est rendue visuellement sous forme de "bloc" (en anglais on parle du [box model](https://www.w3schools.com/css/css_boxmodel.asp)).  

![Le bloc](css-block.png)  

On peut contrôler les dimensions et les espacements de ce bloc :   

- `width`/ `height` : dimensions de largeur et hauteur 
- `border`: contrôle la bordure. Par exemple: `border:1px solid #FF0000;` crée un bord fait d'un trait continu (`solid`) rouge `#FF0000` et de 1px d'épaisseur
- `padding` : l'espace entre le contenu du bloc et son contour (le `border`). Le padding "gonfle" le bloc.  
- `margin` : l'espace autour du bloc, à l'extérieur de lui. Le margin distancie le bloc de son entourage.  

### Les sélecteurs en CSS (part 2) : 
#### Les plus courants
Le plus souvent, on sélectionne les éléments à styliser via l'attribut `class` (`.nom-de-la-classe`) et `id` (`#nom-de-lid`).  

#### Tous les autres sélecteurs
 
-  `+` et `>` 
-  	Sélectionner via l'attribut `[attribute]`
-   Il y en a quelques autres. Pour te faire une idée de ce qu'ils permettent, va lire la petite [doc officielle](https://www.w3schools.com/cssref/css_selectors.asp), puis joue à [CSS Diner](http://flukeout.github.io/)
		
### Concept 3: le positionnement en CSS
Le CSS te permet de définir le positionnement visuel des éléments. C'est probablement le plus riche et donc le plus complexe, car les manières de contrôler le positionnement a eu une histoire plutôt compliquée. Il y a longtemps fallu utiliser des *hacks*. Les choses sont plus stables maintenant, surtout s'il ne faut pas supporter les utilisateurs coincés sur internet explorer 9...  Mais reprenons les choses à leur commencement.
 
#### Comprendre le flux

Chaque bloc html hérite (= "reçoit par défaut") d'une propriété "display" qui est soit : `display: inline | inline-block | block`  et s'affiche en fonction de son ordre d'apparition dans le fichier html. C'est ce que l'on appelle le **flux de positionnement naturel** ou plus simplement le **flux**.

-  Théorie interactive : https://codepen.io/pixeline/pen/QvrbPv 
-  Exercice : un menu horizontal https://codepen.io/pixeline/pen/PmdPYL 
-  Exercice : une grille https://codepen.io/pixeline/pen/aWavWq  
-  `float` va laisser le block flotter sur le block suivant (au lieu de le pousser à la ligne)



#### Sortir du flux 

Le flux est le comportement par défaut. Tu peux avoir besoin qu'un élément sorte du flux de position. 

`position : static | relative | absolute | fixed ;`   

La propriété `position` permet de positionner un élément n'importe où (via les propriétés `top` et `left`), à partir des coordonnées de son premier parent en `position: relative` ou `static`. [Expérimente via ce Pen](https://codepen.io/pixeline/pen/vmzNjw?).

#### Aller plus loin 
Plus d'informations sur le positionnement CSS: http://fr.learnlayout.com


## 3. Web fonts

Par défaut, le navigateur utilise les polices de caractères installées sur l'ordinateur du client. Cependant, tu peux utiliser des polices de caractères spécifiques : les **webfonts**.

**Exercices :**

- Va sur [Google Webfonts](https://fonts.google.com/): change la police de caractère de ton document à celle-ci : Open Sans. Si tu n'y arrives pas, [fais d'abord cet exercice](https://d157rqmxrxj6ey.cloudfront.net/chadsansing/20997/) (clique sur le bouton "remix").
- Choisis une autre police pour les titres, suffisamment différente.

## 4. Outils utiles

- Élimine le css utilisé par défaut par les navigateurs ([reset.css](https://www.alsacreations.com/astuce/lire/36-reset-css.html)), ou pars sur une base normalisée ([normalize.css](https://github.com/necolas/normalize.css))  
- Vérifie que ton HTML est **valide** via le [validateur du w3c](https://validator.w3.org/)
- Vérifie que ton HTML permet **une bonne SEO organique**, via d'autres outils comme le [Google Lighthouse Test](https://developers.google.com/web/tools/lighthouse/) 
- Installe [Emmet](https://emmet.io/) dans ton éditeur de code.

### Crédits

Alexendre Plenneveaux, Becode Bruxelles.
