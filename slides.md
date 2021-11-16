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
  - Dynamique en monolitique
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
L'inpecteur permet de comprendre tout ce qu'il se passe dans le navigateur entre le code que l'on écrit et l'affiche qui est fait !
-->

---
layout: image-right
image: https://images.unsplash.com/photo-1455218873509-8097305ee378?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=687&q=80
---

# Les navigateurs

- Implémentent les spécifications différemment
- Permettent l'interprétation de l'ensemble du code et la visualisation de notre page
- Continnent l'inspecteur


<div class="abs-bl m-6">
  <a href="https://caniuse.com" target="_blank">Can I Use</a>
  -
  <a href="https://developer.mozilla.org/en-US/" target="_blank">MDN</a>
</div>

<!--
Il est important de difféncier différents types de navigateurs et de comprendre leurs constructions.

- IE, mort et le support est arrêté par différent outils de développement comme [Vue.js](https://vuejs.org) ou [WordPress](https://wordpress.com)
- Edge, Chrome, Opera utilise chromium et sont donc tous similaires. Microsoft, Google et Opera ajoutent une sur-couche pour permettre l'utilisation de leurs services.
- Safari et les navigatoires doivent utiliser web-kit et donc ils sont tous similaires.
- Chrome for Android et la plus part des navigateurs sur android utilise Blink

La différence entre toutes ces catégories est dans l'implémentation des fonctionnalités, parser HTML, CSS JS et moteur de rendu CSS et moteur JS.

Du coup, tous les navigateurs se sont pas identiques et des préfix doivent parfois être utilisé. Pour connaître l'implémentation des fonctionnalités, il est recommandé d'utiliser [caniuse](https://caniuse.com).
-->

---
layout: image-left
image: https://images.unsplash.com/photo-1508669232496-137b159c1cdb?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=688&q=80
---

# L'inspecteur

- Insdipensable
- Permet d'analyser son projet en observant
  - Les élements
  - Les scripts
  - Le réseau
  - Les sources
  - ...


<!-- 
Indispensable notamment une fois qu'on a gouté à d'autres langages qui n'ont pas un outil comme celui-ci.

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

Pour les sélecteurs, il faut parler

Pour display, position et z-index, on utilisera différentes boites pour montrer l'imbrication et le fonctionnement des différentes règles.

Pour flex et grid, on verra des exemples simples de mise en pages. Le TP permettra de compléter et de faire une mise en pratique sur du cas concret !
-->

---
layout: cover
background: https://images.unsplash.com/photo-1483728642387-6c3bdd6c93e5?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1476&q=80
---

# Un TP pour tout matriser
The Journey

[Page à réaliser](https://the-journey.web-beginner.esteban-soubiran.site)

<!--
Permet d'aborder l'ensemble des éléments vues précédemments. Aussi, ça permet de faire un hover et donc d'aborder les pseudos classes.
-->

---
layout: end
text: fin
---

<!-- 
Dans les cours suivants, il y a aura un approfondissement du CSS via les pseudos classes et les @rules. On passera aussi sur l'intégration de maquettes responsives en étant mobile first.

Puis, on pourra commencer à voir les bases du javascript.
 -->
