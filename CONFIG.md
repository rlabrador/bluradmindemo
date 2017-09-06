
# Test du BlurAdmin Angular admin panel front-end framework

Voici quelques erreurs rencontrées lors de l'installation et le paramétrage...
## npm install
retourne
[        ..........] - fetchMetadata: sill fetchPackageMetaData Error: unable to verify the first certificate

## npm config set registry

A la suite d'erreur de config et d'erreur de certificat :
Passons les commandes :
>npm config set registry http://registry.npmjs.org/

des ERR apparaissent conseillant de remettre à vide 
>npm config set registry   

(notemment sur tar2.xx.gz)
(Pb de firewall !! Barakuda)

>npm install

puis

>gulp serve

## Créer des Pages
Blur admin uses Angular UI router for navigation. That means to create new page you need to basically configure ui-router state.
https://akveo.github.io/blur-admin/articles/013-create-new-page/



## Amelioration de l'usage des CSS par la précompilation par gulp des fichiers .scss (Compass) 

Il existe de vrais améliorations apportées par l'emploi de Compass sur du CSS3.
l'API de gestion des CSS se fait grâce à CSS3
Si l'on a :

****************
<div class="container">
  <div class="span-15 prepend-1 colborder">
    <div class="span-7 last">
      <h3>Title</h3>
      <p>Bla bla</p>
    </div>
  </div>
</div>

****************


archaïques structures en table (vous me pardonnerez de ne pas utiliser d’exemple pour l’illustrer)
Grace à la compilation de compass, désormais votre framework CSS est dissocié du DOM.
Les classes spécifiques de blueprint (.span-15, .prepend-1,…) peuvent être appelé à l’aide de mixin directement dans le SCSS.

****************
<pre><code>

.main {
    @include span(15);
    @include prepend(1);
    @include colborder(1);
}
.article {
    @include span(7);
    @include last() ;
}
</code></pre>
****************



<div class="container">
  <div class="main">
    <div class="article">
      <h3>Title</h3>
      <p>Bla bla</p>
    </div>
  </div>
</div>

****************


Pour aller plus loin avec Mixins, Include et Extends en SCSS
http://www.bugz.fr/2012/11/css-les-doigts-dans-le-nez-avec-compass/
