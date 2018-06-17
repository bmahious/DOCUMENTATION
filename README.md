# Documentation


### HTML5

HTML (HyperText Markup Language) est le bloc de construction le plus basique du Web. Il décrit et définit le contenu d'une page Web avec la mise en page de base de la page Web. D'autres technologies que le HTML sont généralement utilisées pour décrire l'apparence / la présentation d'une page Web (CSS) ou la fonctionnalité / comportement (JavaScript).

"HyperTexte" fait référence aux liens qui relient les pages Web les unes aux autres, soit sur un seul site Web, soit entre des sites Web. Les liens sont un aspect fondamental du Web. En téléchargeant du contenu sur Internet et en le reliant à des pages créées par d'autres personnes, vous devenez un participant actif sur le Web.

HTML utilise le "balisage" pour annoter du texte, des images et d'autres contenus à afficher dans un navigateur Web. Le balisage HTML inclut des "éléments" spéciaux tels que <head>, <title>, <body>, <entête>, <footer>, <article>, <section>, <p>, <div>, <span>, < img>, <aside>, <audio>, <canvas>, <datalist>, <détails>, <embed>, <nav>, <sortie>, <progression>, <vidéo> et bien d'autres.

Les balises HTML sont insensibles à la casse. Autrement dit, ils peuvent être écrits en majuscules, en minuscules ou en mélange. Exemple La balise <title> peut être écrite comme <Title>, <TITLE> ou de toute autre manière.

### CSS3
(CSS) Cascading Style Sheets est un langage de feuille de style utilisé pour décrire la présentation d'un document écrit dans un langage de balisage comme HTML. Il s'agit d'une technologie de base du World Wide Web, aux côtés de HTML et JavaScript.
CSS3 est la dernière évolution du langage Cascading Style Sheets et vise à étendre CSS2.1. Il apporte beaucoup de nouveautés tant attendues, comme des coins arrondis, des ombres, des dégradés, des transitions ou des animations, ainsi que de nouvelles mises en page comme des multi-colonnes, des boîtes flexibles ou des mises en réseau. Les parties expérimentales sont préfixées par le fournisseur et doivent être évitées dans les environnements de production, ou utilisées avec une extrême prudence car leur syntaxe et leur sémantique peuvent changer à l'avenir.

* structure
* Selecteur (div, .nomDiv, .#id)
* Proprieté (ex. color)
* Attribut (ex. red)

Voici la structure minimale d'une page HTML:
```html
<!DOCTYPE html>
  <html>
    <head>
      <meta charset="utf-8">
      <title>HTML basics</title>
    </head>
    <body>
    </body>
  </html>
```

```html
<!-- mainList = Block -->
<!-- --xmas = Modifier -->
<ul class="mainList mainList--xmas">
  <!-- __item = Element -->
  <li class="mainList__item">
    <!-- __itemLink = Element -->
    <a class="mainList__itemLink mainList__itemLink--isActive" href="/home">Home</a>
  </li>
  <!-- __item = Element -->
  <li class="mainList__item">
    <!-- __itemLink = Element -->
    <a class="mainList__itemLink" href="/home">About</a>
  </li>
  <!-- __item = Element -->
  <li class="mainList__item">
    <!-- __itemLink = Element -->
    <a class="mainList__itemLink" href="/home">Works</a>
  </li>
</ul>
```
### SCSS/SASS

* SCSS

  * Possibilité d'embriquer les selecteurs pour respecter le niveau de hiérarchie
  * Création de conditions, boucles et mixins (responsive)
  * Possibilité d'utiliser des variables

```
.jeSuisParent{
  color: $someColor; // VARIABLE

.jeSuisEnfant {
  color: yellow;
  }
}
```

* SASS :
Sass (Syntactically Awesome Stylesheets) est un langage de génération de feuilles de style initialement développé par Hampton Catlin et Nathalie Weizenbaum.
Sass est un langage de feuilles de style en cascade (CSS). C'est un langage de description qui est compilé en CSS. SassScript est un langage de script pouvant être utilisé à l’intérieur du code Sass. Deux syntaxes existent. La syntaxe originale, nommée « syntaxe indentée », est proche de Haml. La nouvelle syntaxe se nomme SCSS. Elle a un formalisme proche de CSS.

Mêmes carcatéristiques que le SCSS, mais différences à niveau syntaxique: alors que le SCSS respecte l'utilisation des accolades et des points virgules comme en CSS classique, en SASS il n'y a ni d'accolades ni de points virgules, ainsi la hiérarchie est gerée par l'indentation (comme en PUG, voir ci-dessus).


### Sites de veilles

* [Medium](https://medium.com)
* [Awwwards](https://www.awwwards.com)
* [Codepen](https://codepen.io)
* [JDN](https://www.journaldunet.com/)
* [UX Planet](https://uxplanet.org/)

### Sites indispensables
* [W3C](https://www.w3.org/)
* [MDN](https://developer.mozilla.org/fr/)
Exemple en SCSS :
```css
.mainList {
  display: flex;
  justify-content: space-between;
  &--xmas {
    background: green;
  }
  &__item {
    list-style: none;
  }
  &__itemLink {
    color: red;
    &--isActive {
      color: white;
    }
  }
}
```

Exemple en CSS du rendu :
```css
.mainList {

}
.mainList--xmas {

}
.mainList__item {

}
.mainList__itemLink {

}
.mainList__itemLink--isActive {

}
```


## Font-Face

Grâce à @font-face on peut utiliser des polices de caractère non-standard, c’est-à-dire
des polices de caractère autre que celles considérée comme étant 100% compatible
à tous les navigateurs pour le web. (Arial, Helvetica, Times New Roman, Times,
Courier, Verdana, etc.).
En permettant aux auteurs de fournir leurs propres polices, il n'est plus nécessaire de
dépendre uniquement des polices qui sont installées sur les postes des utilisateurs.
La règle @font-face peut être utilisée au niveau global d'une feuille de style et
également au sein d'un groupe lié à une règle @ conditionnelle.


@font face
Définition :
C’est une règle qui permet aux utilisateurs d’intégrer des différentes polices d’écritures qui
sont pas préinstaller sur leurs système, tout en les téléchargent depuis un navigateur. En
d’autres termes, c’est une réponse du CSS aux besoins des webdesigners.

Rôle:
@font face est une typographie qu’on intègre dans la partie style dans nos fichiers CSS. Son
rôle est de transformer le texte souhaité au format demandé par l’utilisateur.

Utilisation :
• Ecrire un texte dans notre fichier HTML sous format : <P>NOTRE TEXTE < /P> par exemple :
<P>je suis un paragraphe < /P> ;
• Télécharger la police qu’on veut intégrer dans notre ficher CSS par exemple « the blacklist »;
• Aller dans le fichier CSS pour intégrer la police tout en incluant @font face, font
family « name », src, url (format.woff)... ;
• Et enfin cibler le paragraphe <P>.
➢ EXEMPLE :
❖ @font face {
Font family : ‘ma police’ ;
src : url ('the_blacklist-webfont.woff2') format('woff2'),
url('the_blacklist-webfont.woff') format('woff');
font-weight: normal;
font-style: normal;
}

• Puis en cible le paragraphe <P> avec :
P {
Font family : ’ma police’ ;
}

✓Et on aura le résultant.



## Pseudo attributs

Les pseudo attributs `before` et `after` permettent de créer des noeuds HTML en CSS.
Ils sont essentiellement utilisés pour ajouter des ornements, des décorations ... On
peut bien entendu faire des animations avec, les positionner par rapport à leur parent
(relative / absolute). **Ils doivent obligatoirement avoir un `content: ''`**
afin de s'afficher.

```html
<section class="cover">
  <h1 class="cover__mainTitle">Présentation des pseudo-attributs</h1>
</section>
```

```css
.cover {
  background: #FDFDFD;
  padding: 20px;
  &__mainTitle {
    text-align: center;
    font-size: 24px;
    color: green;
    position: relative;
    &::before,
    &::after {
      position:absolute;
      content: '';
      display: block;
      width: 50px;
      height: 50px;
      background: green;
      top: 0;
    }
    &::before {
      left: 0;
    }
    &::after {
      right: 0;
    }
  }
}
```

Les pseudo attributs `first-child`, `last-child` et `nth-child(an+b)` permettent de cibler un élément qui est le premier/dernier/nombre élément fils par rapport à son élément parent.

```html
<nav class="navigation">
  <ul class="mainList">
    <li class="mainList_item">Home</li>
    <li class="mainList_item">Works</li>
    <li class="mainList_item">About</li>
    <li class="mainList_item">Contact</li>
    <li class="mainList_item">Social</li>
  </ul>
</nav>
```

```css
.mainList_item {
  text-decoration : none;
  font-size: 20px;
  color: #000;
  &:first-child {
    color: red;
  }
  &:nth-child(3) {
    color: green;
  }
  &:last-child {
    color: blue;
  }
}
```

## REM, EM, %, VW Sizing

### EM
* Relative à la taille de son parent direct.

```css
.cover {
  font-size: 100%;
  /* 100% = 16px */
  &__mainTitle {
    /* 1em = 16px / .8em =/= 16px */
    font-size: .8em;
  }
}
```

### REM

* Le REM est basé sur la taille de la racine (soit la balise <html>) qui, par défault a une valeur de 16px.
Afin d'éviter tout calcul, il est nécessaire de l'écraser en donnant une base de 10px soit 62.5%.
* Le REM est intéressant à utiliser si les media-queries employées sont en rem également. Cela vous permettra
de garder des proportions égales lorsqu'on va redimensionner la page.
* Ses proportions seront également gardées quand l'utilisateur zoomera dans votre page.

```css
html {
  /* 62.5% === 10px */
  font-size: 62.5%;
}
.mainTitle {
  /* 1.6rem == 16px */
  font-size: 1.6rem;
  /* 32rem === 320px */
  width: 32rem;
}
```

### VW(idth) / VH(ieght)

* Unités relatives à la taille de votre écran (peu importe le device)
* Attention au VH et à son contenu. 100vh === 100vh quoi qu'il arrive.
* VW : très utile pour les interfaces fluides.

## Responsive, Media Queries les plus utilisées :

* Sera sur toutes les résolutions
```css
.header {
  height: 400px;
}
```

* Media queries pour mobile
```css
@media (max-width: 480px) {
  /* Affichage sur mobile uniquement */
  .nom-de-class {

  }
}
```

* Media queries pour tablette
```css
@media (max-width: 768px) {
  /* Affichage sur tablette uniquement */
  .nom-de-class {

  }
}
```

* Media queries pour desktop
```css
@media (max-width: 1366px) {
  /* Affichage sur desktop uniquement*/
  .nom-de-class {

  }
}
```

* Media queries pour desktop-large
```css
@media (min-width: 961px) {
  /* Affichage sur desktop-large uniquement*/
  .nom-de-class {

  }
}
```


## Flexbox Grid

* Télécharger [flexboxgrid](http://flexboxgrid.com/) et mettre dans un dossier (.min.css) css avec le style.

* **Ne jamais utilisé de margin ou padding sur les class="col-xxx" quand on utilise une grille**

* col-xs > desktop / col-sm > tablette / col-lg > téléphone etc.
* offset permet de "sauter" des collonnes.

```html
<div class="container">
  <div class="row">

    <div class="col-xs-6 col-lg-4" >
      <h2> Titre 1</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Temporibus fugit eligendi quo quia praesentium. Nam facere, est modi enim corporis perspiciatis, provident cumque.</p>
    </div>

    <div class="col-xs-6 col-lg-4">
      <h2>Titre 2</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolore ad provident molestiae reprehenderit explicabo aliquid atque incidunt unde amet.</p>
    </div>

    <div class="col-xs-6 col-lg-4">
      <h2>Titre 3</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laborum rerum eum, quae voluptatum omnis aut eligendi, placeat ullam suscipit!</p>
    </div>

    <div class="col-xs-6 col-lg-6">
      <h2>Titre 4</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perferendis, eos aliquam sed quas optio porro architecto doloribus dicta. Rem voluptatibus corporis, molestias eos atque, sint!</p>
    </div>

    <div class="col-xs-12 col-lg-5 col-lg-offset-1">
      <h1>Titre 5</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deserunt error hic, autem sapiente delectus magni expedita. Eveniet blanditiis quod provident.</p>
    </div>

  </div>
</div>
```


## Parcel-bundler (installation)

Pré requis : node.js

Dans un dossier de dévelloppement, ecrire depuis FastShell :

* mkdir parcel-bundler -> cd parcel-bundler
* npm init
* npm install -g parcel-bundler
* mkdir src -> cd src
* touch index.html index.js
* mkdir styles -> cd styles
* touch styles.scss
* mkdir global && mkdir components && mkdir mixins
* touch global/`_variables.scss` && touch global/`_reset.scss` && touch mixins/`_forsize.scss`
* cd .. -> npm install
* touch .postcssrc
* npm install autoprefixer
* touch .babelrc
* npm install -D babel-preset-env

Pour lancer le serveur :
* npm start


## GitHub :

Récupérer un repositories :
* git clone https://lien-du-repo.git

Linker son dossier de travail à un répo GitHub :
* git remote add origin (url du github)

**Travailler sur le master est déconseillé, voir interdit selon les projets pour cela utiliser les branchs :**

* git checkout -b (nom de la branch) : créer une nouvelle branch
* git checkout (nom de la branch) : changer de branch

Push un projet sur GitHub :

* git add .
* git commit -m "message"
* git push origin (nom de la branch )

Pull un projet de GitHub :

* git pull origin (nom de la branch)


## Liens utiles :
* [Caniuse](https://caniuse.com/) : "c'est compatible partout ou pas?"
* [FrontEndQuizz](https://github.com/h5bp/Front-end-Developer-Interview-Questions)
* [CssNext](http://cssnext.io/)
* [MDN web docs](https://developer.mozilla.org/fr/)
