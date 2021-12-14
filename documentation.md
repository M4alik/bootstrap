# Introduction à Bootstrap

## Les colonnes

Il faut garder en tête que Bootstrap va permettre d'organiser un élément parent de notre document html en 12 colonnes. Ensuite, ses éléments enfants pourront être répartis entre ces 12 colonnes. Par exemple : supposons quune balise *section* contiennent des balises *articles*. Nous pourrons disposer chacune de ces balises *article* à l'intérieur de *section* comme bon nous semble. Pour celà il suffit d'applique à la balise *article* voulue, la classe `code` suivie d'un tiret et d'un chiffre correspondant au nombre de colonnes que l'on veut appliquer à l'article.

```html:
<section class="container">
    <article class="col-4">
        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
    </article>

    <article class="col-4">
        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
    </article>

    <article class="col-4">
        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
    </article>
</section>
```
Ici chaque balise *article* occupera 4 colonnes sur 12, soit 1/3 de la largeur totale de l'élément parent (*section*)

Il est possible de préciser à la classe `code` le nombre de colonne à occuper en **fonction de la largeur de l'écran**. On parle de breakpoints :
- inférieur à 576px
- entre 576 et 767px (`sm`)
- entre 768 et 992px (`md`)
- entre 993 et 1200px (`lg`)
- entre 1201 et 1400px (`xl`)
- supérieur à 1400px (`xxl`)

Il suffira d'écrire par exemple `col-md-6` pour dire à un élément d'occuper 6 colonnes de l'élément parent sur une taille d'écran comprise entre 768 et 992 px. On peut combiner ces classes entre elles pour rendre les éléments *responsive*.

## Flexbox
On peut appliquer *flexbox* à un élément parent pour permettre d'organiser ses éléments enfants.
- En donnant la classe `row` à un élément, celui-ci acquiert `display: flex;` et `flex-direction: row;`.
- En donnant la classe `column` à un élément, celui-ci acquiert `display: flex;` et `flex-direction: column;`
- en donnant la classe `align-items-start` à un élément, celui-ci acquiert en plus `align-items: flex-start;`. (on peut utiliser aussi `end`, `center`, `stretch`, `baseline`)
- en donnant la classe `justify-content-start` à un élément, celui-ci acquiert en plus `justify-content: start;`. (on peut utiliser aussi `end`, `center`, `between`, `around`, `evenly`).

[retour à l'exercice](README.md)