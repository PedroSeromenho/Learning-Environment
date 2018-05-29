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
#### Sortir du flux 

Le flux est le comportement par défaut. Tu peux avoir besoin qu'un élément sorte du flux de position. 

`position : static | relative | absolute | fixed ;`   

La propriété `position` permet de positionner un élément n'importe où (via les propriétés `top` et `left`), à partir des coordonnées de son premier parent en `position: relative` ou `static`. [Expérimente via ce Pen](https://codepen.io/pixeline/pen/vmzNjw?).

**Exercices :**  

- Réalise une [notification d'interface](https://codepen.io/pixeline/pen/dWqMxe)
- [exercice de position absolue](https://codepen.io/pixeline/pen/JNaKJv) 

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
