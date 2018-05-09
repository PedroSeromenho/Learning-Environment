
# 1. Le Markdown c'est quoi? 
Markdown est un langage de balisage léger créé par John Gruber en 2004. Son but est d'offrir une syntaxe facile à lire et à écrire. Un document balisé par Markdown peut être lu en l'état sans 
donner l’impression d'avoir été balisé ou formaté par des instructions particulières.

Un document balisé par Markdown peut être converti en HTML ou en autres formats. Bien que la syntaxe Markdown ait été influencée par plusieurs filtres de conversion de texte existants vers HTML — dont Setext1, atx2, 
Textile, reStructuredText, Grutatext3 et EtText4 —, la source d’inspiration principale est le format du courrier électronique en mode texte.

## 2. Evolution.

Depuis sa création originelle par Gruber, Markdown n'a pas connu d'évolution notoire de la part de ses auteurs. De plus, ce format n'a jamais été formellement standardisé.

Un certain nombre de variantes ont donc été développées par d'autres, afin de pallier ce qui a été perçu comme des limitations inhérentes à une syntaxe très simplifiée.

À titre d'exemples, on pourra citer MultiMarkdown et GitHub Flavored Markdown15. Ce dernier est utilisé pour les articles et la documentation sur Github lui-même, mais a également été largement adopté sur plusieurs 
éditeurs de texte supportant le format Markdown au niveau de la coloration syntaxique ou de la prévisualisation.

Il existe également des greffons pour de nombreux logiciels populaires, tels que « Markdown Here » pour Firefox et Chrome, et le système de gestion de contenu WordPress intègre désormais quelques éléments de ce 
langage nativement depuis la version 4.3.

L'initiative Common Mark16 vise à pallier le manque de standardisation et les ambiguïtés du format.

Pour plus d'informations [c'est ici](https://fr.wikipedia.org/wiki/Markdown)

### 3. La synthaxe de Markdown. 

 * Titre : 
	* h1: #
	* h2: ##
	* h3: ###

 * Paragraphe : 
	 Paragraphe 1 
	
	 Paragraphe 2
 
 * Styles de caractères : 
	* *Italic characters* 
	* _Italic characters_
	* **bold characters**
	* __bold characters__
	* ~~strikethrough text~~
 
 * Listes non ordonnée :
	* *  Item 1
	* *  Item 2
	* *  Item 3
    *	* *  Item 3a
    *	* *  Item 3b
    *	* *  Item 3c

 * Liste ordonnée : 
	* 1. Item 1 
	* 2. Item 2 
	* 3. Item 3
		*	1. Item 1.1 
		*	2. Item 2.1
		*	3. Item 3.1
 
 * Tableaux : 
	
	| Titre 1       |     Titre 2     |        Titre 3 |
	| :------------ | :-------------: | -------------: |
	| Colonne       |     Colonne     |        Colonne |
	| Alignée à     |   Alignée au    |      Alignée à |
	| Gauche        |     Centre      |         Droite |

 
 * Liens : 
	* [Lien vers Markdown](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

 * Image : 
	* [Dark wed](dark11.jpg)


``` javascript 

	<script>
	document.getElementById("demo").innerHTML = "Hello JavaScript!";
	</script>

```

# Markdown


![Image of Markdown](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)

## Historique

Markdown est un [langage de balisage léger](https://fr.wikipedia.org/wiki/Langage_de_balisage_l%C3%A9ger) **créé par John Gruber** en 2004. Son but est d'offrir une [syntaxe](https://fr.wikipedia.org/wiki/Syntaxe) facile à *lire* et à *écrire*. Un document balisé par Markdown peut être lu en l'état sans donner l’impression d'avoir été balisé ou formaté par des instructions particulières.

## Utilisation

* Un document balisé par Markdown peut être converti en HTML ou en autres formats.
* Bien que la syntaxe Markdown ait été influencée par plusieurs filtres de conversion de texte existants vers HTML — dont [Setext](https://fr.wikipedia.org/wiki/Setext), atx, [Textile](https://fr.wikipedia.org/wiki/Textile), [reStructuredText](https://fr.wikipedia.org/wiki/ReStructuredText), Grutatext et EtText.
* La source d’inspiration principale est le format du [courrier électronique](https://fr.wikipedia.org/wiki/Courrier_%C3%A9lectronique) en mode texte.

## Exemples

1.	[Formatage](https://fr.wikipedia.org/wiki/Markdown#Formatage)
2.	[Listes](https://fr.wikipedia.org/wiki/Markdown#Listes)
3.	[Titres](https://fr.wikipedia.org/wiki/Markdown#Titres)
4.	[Tableaux](https://fr.wikipedia.org/wiki/Markdown#Tableaux)
5.	[Liens](https://fr.wikipedia.org/wiki/Markdown#Liens)
6.	[Images](https://fr.wikipedia.org/wiki/Markdown#Images)

![Alt gif](https://media.giphy.com/media/vFKqnCdLPNOKc/giphy.gif)


## Mise en Œuvre

Plusieurs mises en œuvre existent et ce dans différents langages de programmation :
* Perl5
* PHP6
* Ruby7
* Python8
* Java9
* C#10
* Haskell11
* Gambas
* R12
* JavaScript13
  * Strapdown.js14.
  * Version 2.0 de Swift aussi possible dans ces playgrounds.


Pros | Contre
------------ | -------------
Antony | Mohamed Ali
Liliane | Geofrey



  ```javascript
  function fancyAlert(arg) {
    if(arg) {
      $.facebox({div:'#foo'})
    }
  }
  ```

=======
## Bienvenue dans le Markdown
-----------------------------

### Qu’est-ce que Markdown ?
----------------------------
**Markdown** est un système d’édition et de *formatage de texte* ; c’est à la fois une **syntaxe**, un script de conversion texte → HTML et un format de fichier. Il est couramment utilisé pour les fichiers de documentation d’un projet ou d’un jeu de données -souvent nommé readme.md.


Il est stocké au format texte classique et est plus léger que sa version interprétée puisqu’il ne contient pas les balises html.

La philosophie du système veut que le texte écrit soit lisible sans interpréteur particulier en mode texte. Il est léger et épuré de l’essentiel de la verbosité d’un language balisé. Les éléments de syntaxe sont des caractères de ponctuation qui font sens visuellement même non convertis.


Une fois converti, le navigateur web (qui joue alors le rôle d’interpréteur) en rendra la lecture plus claire.


Les fichiers sont généralement enregistrés avec l’extension .md (ou .markdown ) pour indiquer aux interpréteur la nature du texte qu’il vont lire ; mais ça n’a rien d’obligatoire.



Comme le résultat sera exporté en HMTL, vous pouvez tout à fait introduire directement des balises HTML dans votre texte ; mais celui-ci deviendra moins lisible et ne pourra plus être édité par quelqu’un ne maîtrisant pas le HTML. Attention, le formatage markdown ne sera pas appliqué à l’intérieur de ces balises.



### Markdown: La Syntaxe:

#### les titres :
   pour utiliser on utilisera cette syntaxe :

# Titre 1     
## Titre 2       
### Titre 3       
#### Titre 4     
##### Titre 5

#### Les paragraphes:
Pour afficher un paragraphe, sautez deux ligne et de taper son texte.


Un seul saut de ligne correspond à un retour chariot et pas à un changement de paragraphe.


#### L’emphase:
Pour formater une partie de votre texte comme emphase, entourez le par des astérisques ou des underscores. Entourer par un signe unique passe en italique (emphase faible : *;) et par un double signe en gras (emphase forte: **;).


Il est possible de combiner les deux. Un double tildes vous permettent de barrer le texte.


À titre personnel, j’utilise plutôt les astérisques, mais c’est une question de goût. La seule chose importante est d’être cohérent dans vos documents.


*italique* , en **bold** ou ~~barrés~~ .


### Listes:
Sauter une ligne avant le début de la liste. puis on ajoute soit un * , + ou un - avant chaque point.
1. Liste désordonné

* Pommes
* Poires
  * Sous élément avec au moins quatre espaces devant.

2. Liste Ordonné

1. mon premier
2. mon deuxième


3. Liste en mode case à coche

- [ ] Case non cochée
- [x] Case cochée

#### Tableau:

On crée des tables en assemblant des - pour les row et | pour les columns

| Titre 1       |     Titre 2     |        Titre 3 |
| :------------ | :-------------: | -------------: |
| Colonne       |     Colonne     |        Colonne |
| Alignée à     |   Alignée au    |      Alignée à |
| Gauche        |     Centre      |         Droite |

#### Liens

utiliser: [texte du lien](url_du_lien "texte pour le titre, facultatif")


exemple: [Becode](https://register.becode.org/)

#### Images

1. images statiques
On utilise: ![GitHub Logo](/images/logo.png)

  ![Cheat sheet](markdown.png)
	![Cheat sheet2](markdown2.png)


2. Images dinamiques ( gif ):

	![Alt Text](https://media.giphy.com/media/vFKqnCdLPNOKc/giphy.gif)

#### un bout de code:
Mettre son code entre deux ( ``` ``` )


```javascript
  <script type="text/javascript" >
    window.alert("Hello World!");

    alert("Hello World!");
   </script>
```

