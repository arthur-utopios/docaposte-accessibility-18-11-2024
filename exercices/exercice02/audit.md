---
title: Audit AlloCiné
page: https://www.allocine.fr/film/fichefilm_gen_cfilm=269223.html
date: 19-11-2024
---

# Audit de AlloCiné

## Etape 1 : technologies d'assistances

- Lors du parcours de la page, barre de navigation avec des boutons sans focus ce qui empêche de connaître notre position sur le site
- Bouton envie de voir sans focus
- Pas de sélection au clavier sur l'élément rédiger ma critique
- Bordure de focus très fine et différente selon les éléments
- Lien sans `aria-label` le lecteur ne peut donc pas l'identifier

```html
<a
  class="xXx button button-sm button-club-300"
  href="/article/fichearticle_gen_carticle=1000112280.html"
>
</a>
```

- Balise div utilisé comme un bouton mais qui n'est pas accessible car pas de tabindex ni de aria-label

```html
<div
  class="bam-cell bam-review js-user-review-link"
  data-content="Rédiger ma critique"
  data-classes="button icon icon-pen"
  data-entity-id="TW92aWU6MjY5MjIz"
>
  <div class="button icon icon-pen">Rédiger ma critique</div>
</div>
```

- NDVA lit deux fois la même chose à cause du aria-label spécifié dans la div parente

```html
<div
  aria-label="Rechercher un film, une série, une star..."
  class="container-input-autocomplete"
  role="search"
>
  <div class="container-input-mask">
    <input
      class="header-search-input"
      id="header-search-input"
      name="q"
      type="text"
      autocomplete="off"
      placeholder="Rechercher un film, une série, une star..."
      aria-autocomplete="both"
      aria-label="search"
      aria-multiline="false"
      role="textbox"
      value=""
    />
  </div>
</div>
```

## Etape 2 : interactions avec le contenu HTML

- Présence des principales balises sémantiques : header, main footer
- Présence d'image sans attribut alt ou aria-hidden="true" ou role="presentation" ou role="none"
- Couleur à revoir : #FECC00 sur fond #FFFFFF
- Présence de balises aria

## Etape 3 : Standard ARIA

- Présence de balises aria plutôt bien arrangées, utilisation correcte
- 42 aria
  - 30 aria label
  - 7 tabindex
  - 3 aria hidden
  - 2 autres aria

## Etape 4 : Outils d'inspection

D'après WAVE :

- 1 lien vide
- 6 Images sans texte alternatif et non visible
- 14 erreurs de contrastes liées à du texte sur des Images
- 148 alertes

## Etape 5 : Images

- Beaucoup d'images sans alt

## Etape 6 : iFrame

- Présence de beaucoup trop de iframe (ralentissement du site, pas forcément accessible)
- Pas de title sur les iFrame

## Etape 7 : Multimédia

- Présence de sous-titres
- Utilisation de Dailymotion qui est accessible au clavier + sous-titre

## Etape 8 : Tableaux

Pas de tableaux présents

## Etape 9 : Liens

- Un lien non accessible

```html
<a
  class="xXx button button-sm button-club-300"
  href="/article/fichearticle_gen_carticle=1000112280.html"
>
</a>
```

---

## Recommandations

- Simplifier l'interface graphique et les menus
- Faire de la publicité moins intrusive
- Réduire le nombre d'iFrame sur le site
- Mieux gérer la gestion des attribut rôle en utilisant des balises accessibles sur les éléments enfants : images
- Ne pas utiliser de div comme bouton pour éviter d'avoir du contenu non accessible
- Ne pas utiliser la primary color jaune sur un fond blanc
