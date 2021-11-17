---
theme: seriph
background: >-
  https://images.unsplash.com/photo-1601302249997-35a818561543?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1470&q=80
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Le développement web
  La première journée d'un long voyage
drawings:
  persist: false
title: Le développement web
titleTemplate: '%s - Estéban Soubiran'
---

# Le développement web
La première journée d'un long voyage

<div class="abs-bl m-6">
11/2021
</div>

<div class="abs-br m-6">
  Par <a href="https://esteban-soubiran.ste" target="_blank">Estéban Soubiran</a>
</div>

---
layout: intro
---

# Estéban Soubiran

<div class="leading-8 opacity-80">
Élève-ingénieur en sécurité informatique<br>
Développeur web dans son temps libre<br>
Passionné par le monde associatif<br>
</div>

<div class="my-10 grid grid-cols-[40px,1fr] w-min gap-y-4">
  <ri-github-line class="opacity-50"/>
  <div><a href="https://github.com/barbapapazes" target="_blank">Barbapapazes</a></div>
  <ri-twitter-line class="opacity-50"/>
  <div><a href="https://twitter.com/soubiran25" target="_blank">@SOUBIRAN25</a></div>
  <ri-user-3-line class="opacity-50"/>
  <div style="white-space: nowrap;"><a href="https://esteban-soubiran.site" target="_blank">esteban-soubiran.site</a></div>
</div>

<img src="/me.webp" class="rounded-full w-40 abs-tr mt-16 mr-12"/>

---
layout: section
---

# Fonctionnement du web
Client / Serveur

<!--
Faire un schéma expliquant le fonctionnement du web et la relation client-serveur.

- Protocole HTTP
  HyperText Transfer Protocole
  Couche 7 du modèle OSI et fonctionne avec IP
  Permet de faire le lien entre le client et le serveur. Le client est à l'initiative des requêtes. La conséquence est que le serveur ne peut pas envoyer de données au client sans que celles-ci soient demandées par le client.
- Stateless
  Après le chargement d'une page web, la connection est terminée
    Le serveur peut gérer chaque demande de manière unique et n'a pas besoin de conserver un état de session pour le client
- Différents modèles pour la création de site et application web
  Solutions: 
  - Statique
    - Vanilla ou web-framework en SSG ou client-side
  - Dynamique en monolithique
  - Séparation du back et du front
  - API REST
    - Vanilla ou web-framework en SSR, SSG ou client-side
-->

---
layout: section
---

# Le navigateur
Et son inspecteur

<!--
Important de comprendre comment fonctionne ses outils de travail

Le navigateur, c'est comme une grande feuille blanche et on va venir y créer des interfaces utilisateurs !
L'inspecteur permet de comprendre tout ce qu'il se passe dans le navigateur entre le code que l'on écrit et l'affiche qui est fait !
-->

---
layout: image-right
image: https://images.unsplash.com/photo-1455218873509-8097305ee378?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=687&q=80
---

# Les navigateurs

- Implémentent les spécifications différemment
- Permettent l'interprétation de l'ensemble du code et la visualisation de notre page
- Contiennent l'inspecteur


<div class="abs-bl m-6">
  <a href="https://caniuse.com" target="_blank">Can I Use</a>
  -
  <a href="https://developer.mozilla.org/en-US/" target="_blank">MDN</a>
</div>

<!--
Il est important de différencier différents types de navigateurs et de comprendre leurs constructions.

- IE, mort et le support est arrêté par différent outils de développement comme [Vue.js](https://vuejs.org) ou [WordPress](https://wordpress.com)
- Edge, Chrome, Opera utilise chromium et sont donc tous similaires. Microsoft, Google et Opera ajoutent une sur-couche pour permettre l'utilisation de leurs services.
- Safari et les navigateurs doivent utiliser web-kit et donc ils sont tous similaires.
- Chrome for Android et la plus part des navigateurs sur android utilise Blink

La différence entre toutes ces catégories est dans l'implémentation des fonctionnalités, parser HTML, CSS JS et moteur de rendu CSS et moteur JS.

Du coup, tous les navigateurs se sont pas identiques et des préfix doivent parfois être utilisé. Pour connaître l'implémentation des fonctionnalités, il est recommandé d'utiliser [caniuse](https://caniuse.com).
-->

---
layout: image-left
image: https://images.unsplash.com/photo-1508669232496-137b159c1cdb?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=688&q=80
---

# L'inspecteur

- Indispensable
- Permet d'analyser son projet en observant
  - Les éléments
  - Les scripts
  - Le réseau
  - Les sources
  - ...


<!-- 
Indispensable notamment une fois qu'on a goûté à d'autres langages qui n'ont pas un outil comme celui-ci.

Il faut faire une démonstration pour chaque onglet de ce que l'on peut y trouver.

- Elements
  Permet d'observer l'ensemble du code HTML et CSS du site
- Console
  Permet d'interpréter du javascript mais aussi d'inspecter le code javascript du site.
- Réseau
  Permet de voir l'ensemble des requêtes réseaux effectuées par le site. Sur l'ensemble des requêtes, on a accès à différentes informations comme les headers.
- Sources
  Permet de voir l'ensemble des fichiers dont le site fait appels. On peut les analyser en regardant le code mais aussi y placer des points d'arrêts pour inspecter les différents variables.
-->
---
layout: section
---

# HTML
HyperText Markup Langage

---

# Langage de balisage

<v-clicks>

- Utilisation de tags pour la sémantique du contenu
  ```html
    <main>
        <h2>This is a level 2 heading</h2>
        <p>This a paragraph inside a p tag ! 💃</p>
        <ul>
          <li>Item 1 🚀</li>
          <li>Item 2 🚌</li>
          <li>Item 3 🚂</li>
        </ul>
    </main>
  ``` 
- Ne permet pas de faire de l'algorithmique
- Ne permet pas de mettre en page son site
- Toutes les références sont dans [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

</v-clicks>

<!-- 
L'HTML permet de donner du sens au contenu de son texte. C'est la signification de "permettre la sémantique".
Pour donner ce sens, on utilise des tags. Il existe de nombreux tags que l'on peut trouver [à cette adresse](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

Rien de mieux que l'inspecteur pour observer l'HTML d'une page web !

La MDN est la bible du développeur web. Vous allez pouvoir y retrouver tout ce dont vous avez besoin.

Faire une mise en pratique
 -->
---
layout: section
---

# Mise en pratique
HTML

---
layout: section
---

# CSS
Cascading Style Sheet

---
layout: image-right
image: https://images.unsplash.com/photo-1502252430442-aac78f397426?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1470&q=80
---

# Langage de mise en page

- Fonctionnement en cascade
- Permet la mise en page du contenu
- Permet la création d'animations et de transitions

<!--
Le fonctionnement en cascade permet d'appliquer une règle à un parent et que celle-ci soit appliquée à tous ses enfants comme la couleur du texte.
-->
---
layout: section
---

# Mise en pratique
CSS

<section class="max-w-md mx-auto mt-12 grid grid-cols-2">
  <div class="flex flex-col space-y-2">
    <span>Colors</span>
    <span>Fonts</span>
    <span>Border</span>
    <span>Margin</span>
    <span>Padding</span>
    <span>Width</span>
    <span>Height</span>
  </div>
  <div class="flex flex-col space-y-2">
    <span>Display</span>
    <span>Position</span>
    <span>Z-Index</span>
    <span>Flex</span>
    <span>Grid</span>
  </div>
</section>

<!--
Pour chacune de ses règles, on va faire une mise en pratique. Dans le même temps, on abordera les sélecteurs.

Pour les sélecteurs, il faut parler de leur fonctionnement et de leurs spécificités.

Pour colors, fonts, border, width, height, margin et padding on passera directement sur un éditeur de code.
Dans le cadre des margins, on rappellera que les margins ne se chevauche pas. 
Pour les margins et les paddings, il faut faire le schémas avec les boites.

Pour display, position et z-index, on utilisera différentes boites pour montrer l'imbrication et le fonctionnement des différentes règles. Des slides permettent de le montrer.

Pour flex et grid, on verra des exemples simples de mise en pages et des slides sont préparées. Le TP permettra de compléter et de faire une mise en pratique sur du cas concret !
Flex permet de faire de l'alignement dans 1 dimension
Grid permet de faire de l'alignement dans 2 dimensions
-->

---

<section>
  <div class="space-y-4 mb-16">
  <h2>Position : Static</h2>
    <div class="border border-gray-100 p-2 space-y-4">
      <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
        Box 1
     </div>
      <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
        Box 2
      </div>
      <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
        Box 3
      </div>
    </div>
  </div>
</section>

- Positionné selon le flow normal du document
- `top`,`bottom`, `right`, `left` et `z-index` n'ont pas d'effet
- Valeur par défaut

<div class="abs-br m-6">
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/position" target="_blank">MDN</a>
</div>

---

<section>
  <div class="space-y-4 mb-16">
    <h2>Position : Relative</h2>
    <div class="border border-gray-100 p-2 space-y-4">
      <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
        Box 1
      </div>
      <div class="relative top-8 left-4 border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
        Box 2
      </div>
      <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
        Box 3
      </div>
    </div>
  </div>
</section>

- Positionné selon le flow normal du document
- `top`,`bottom`, `right`, `left` et `z-index` permet de positionner l'élément relativement à lui-même
- N'affecte pas les autres éléments

<div class="abs-br m-6">
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/position" target="_blank">MDN</a>
</div>

---

<section>
  <div class="space-y-4 mb-16">
    <h2>Position : Absolute</h2>
    <div class="relative space-y-4 border border-gray-100 p-2">
      <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
        Box 1
      </div>
      <div class="absolute top-8 right-1/2 border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
        Box 2
      </div>
      <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
        Box 3
      </div>
    </div>
  </div>
</section>

- Sortie du flow du document
- `top`,`bottom`, `right`, `left` et `z-index` permet de positionner l'élément relativement à un parent positionné

<div class="abs-br m-6">
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/position" target="_blank">MDN</a>
</div>

---

<section>
  <div class="space-y-4 mb-16">
    <h2>Display : Block</h2>
    <div class="space-y-4 border border-gray-100 p-2">
      <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
        Box 1
      </div>
      <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
        Box 2
      </div>
      <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
        Box 3
      </div>
    </div>
  </div>
</section>

- Génère un retour à la ligne avant et après l'élément lorsqu'il est dans le flow du document
- Valeur par défaut

<div class="abs-br m-6">
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/display" target="_blank">MDN</a>
</div>

---

<section>
  <div class="space-y-4 mb-16">
    <h2>Display : Inline</h2>
    <div class="space-y-4 border border-gray-100 p-2">
      <div class="inline border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
        Box 1
      </div>
      <div class="inline border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
        Box 2
      </div>
      <div class="inline border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
        Box 3
      </div>
    </div>
  </div>
</section>

- Ne génère pas un retour à la ligne avant et après l'élément lorsqu'il est dans le flow du document
- Les marges sur y ne sont plus prises en compte

<div class="abs-br m-6">
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/display" target="_blank">MDN</a>
</div>

---
layout: two-cols
---

<section>
  <div class="space-y-4 mb-16">
    <h2>Display : Flex</h2>
    <div class="space-y-4 border border-gray-100 p-2">
      <div class="flex">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
      <div class="flex justify-center">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
      <div class="flex justify-end">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
      <div class="flex justify-between">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
      <div class="flex justify-around">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
    </div>
  </div>
</section>

::right::

<section class="h-full ml-2">
  <div class="space-y-4 h-full">
    <div class="border border-gray-100 p-2 grid grid-cols-5 gap-4 h-full">
      <div class="flex flex-col">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
      <div class="flex flex-col justify-center">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
      <div class="flex flex-col justify-end">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
      <div class="flex flex-col justify-between">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
      <div class="flex flex-col justify-around">
        <div class="border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
          Box 1
        </div>
        <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
          Box 2
        </div>
        <div class="border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
          Box 3
        </div>
      </div>
    </div>
  </div>
</section>

<div class="abs-br m-6">
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/display" target="_blank">MDN</a>
</div>

---

<section>
  <h2>Display : Grid</h2>
  <div class="border border-gray-100 p-2 mt-4">
    <div class="grid grid-cols-5 grid-rows-6 gap-2">
      <div class="col-span-4 border-2 border-teal-600 bg-teal-300 text-black text-center p-4">
        Box 1
      </div>
      <div class="border-2 border-cyan-600 bg-cyan-300 text-black text-center p-4">
        Box 2
      </div>
      <div class="row-start-3 col-start-3 border-2 border-light-blue-600 bg-light-blue-300 text-black text-center p-4">
        Box 3
      </div>
      <div class="row-start-4 col-start-4 col-span-2 row-span-2 border-2 border-blue-600 bg-blue-300 text-black flex items-center justify-center p-4">
        Box 4
      </div>
        <div class="row-start-5 col-span-2 row-span-2  border-2 border-indigo-600 bg-indigo-300 text-black flex items-center justify-center p-4">
        Box 5
      </div>
    </div>
  </div>
</section>

<div class="abs-br m-6">
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/display" target="_blank">MDN</a>
</div>

---
layout: cover
background: https://images.unsplash.com/photo-1483728642387-6c3bdd6c93e5?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1476&q=80
---

# Un TP pour tout maîtriser
The Journey

[Page à réaliser](https://the-journey.web-beginner.esteban-soubiran.site)

<!--
Permet d'aborder l'ensemble des éléments vues précédemment. Aussi, ça permet de faire un hover et donc d'aborder les pseudos classes.
-->

---
layout: end
text: fin
---

<!-- 
Dans les cours suivants, il y a aura un approfondissement du CSS via les pseudos classes et les @rules. On passera aussi sur l'intégration de maquettes responsive en étant mobile first.

Puis, on pourra commencer à voir les bases du javascript.
 -->

---
layout: section
---

# CSS Avancé

---

# Sélecteurs

- Permettent de sélectionner un ou des éléments
- Permettent une sélection très précises et / ou très variées
- Permettent de sélectionner des états des éléments

<br>
<br>

```css
/* Quelques exemples */

.ma_class {} 

.ma_class mon_element {}

#mon_id {}

mon_element:mon_etat {}

@media screen and (min-width: 640px) {}
```

<div class="abs-br m-6 space-x-4">
  <a href="https://flukeout.github.io" target="_blank">CSS Diner</a>
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors" target="_blank">MDN</a>
</div>

<!-- 
Il faut parler des priorités sur les sélecteurs et le poids de chacun. Pour cela, on peut utiliser l'outil de VSCode qui indique le poids total d'une classe dans un fichier CSS.
-->

---
layout: image-right
image: https://images.unsplash.com/photo-1607992922515-7e38329e65d4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1014&q=80
---

# Pseudo-classes

<div class="abs-br m-6 space-x-4">
  <a href="https://flukeout.github.io" target="_blank">CSS Diner</a>
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors" target="_blank">MDN</a>
</div>

<!-- 
Faire une découverte et un exercice sur [CSS Diner](https://flukeout.github.io)
-->

---

# Pseudo-éléments

---
 
# Design Responsive

---

# @rules

---
preload: false
---

# Transition & Animations

---

# Miscellaneous


<!-- 
Pour les variables en CSS, il faut faire une démonstration. Il faut aussi montrer que plus la variable est proche de sa cible, plus elle est prioritaire. Cela permet une redéfinition et un changement de l'élément sans jour sur les classes. Le code est donc plus lisible et plus simple à écrire et à maintenir.
 -->