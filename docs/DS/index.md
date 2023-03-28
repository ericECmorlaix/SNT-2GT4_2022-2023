# Thème 3 : Les données

![](../images/logo_data.png){align=left}
        
L'informatique étant le traitement automatique de données,  ces données constituent la matière première de toute activité numérique.
        
Afin de permettre leur réutilisation, il est nécessaire de les conserver de manière persistante.
        
Les structurer correctement garantit que l’on puisse les exploiter facilement pour produire de l’information.


## Expériences de traitement

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/IJJgcZ2DEs0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

**Découvrir** la manipulation de données sur [la plateforme France-IOI](https://concours.castor-informatique.fr/){target=_blank} avec les codes :

- `7vi35usa` pour l'activité n°1 ;
- `hk3uggux` pour l'activité n°2 ;
- `wvs3ewgc` pour l'activité n°3 ;

OU sur la nouvelle mouture de la plateforme : [Les données structurées et leur traitement](https://parcours.algorea.org/contents/4707-4701-1067253748629066205-653650670442840123/){target=_blank}

???- abstract "Notions et vocabulaire à retenir"

    - Une **collection** est un ensemble d’**objets** (concrets ou abstraits) dont on collecte des **données**, partageant les mêmes **descripteurs**.
    - Un **objet** est un élément de cette **collection**.
    - Un **descripteur** désigne une caractéristique de l’**objet** concerné par la **donnée**.
    - Une **valeur** est l’**information** elle-même, c.a.d. la **donnée**.
    - Le **type** d’une **valeur** est la nature de cette **information**. On ne peut comparer des **données** que si elles sont de même **type**.

    ???- example "Exemple"
        Si on s’intéresse aux **données** gérées par une bibliothèques.

        - L’ensemble des usagers de la bibliothèque est une **collection** ; L’ensemble des livres en est une autre.
        - Chacun des livres est un **objet** de cette **collection**.
        - Le titre comme le numéro ISBN sont des **descripteurs** de la **collection** livres.
        - `9782070319527` est la **valeur** du nombre correspondant au numéro ISBN d'un livre dont le titre à pour **valeur** la chaine de caractères `"Les fleurs du mal"` (nombre et chaine de caractères sont des **types** de **données**).

    - Si une **donnée** concerne une personne, on dit que c’est une **donnée personnelle**. Le règlement général sur la protection des données, **R.G.P.D.**, encadre le traitement des **données personnelles** sur le territoire de l'Union européenne.
    - Une **métadonnées** est une **donnée** qui renseigne sur une **donnée**. Un fichier numérique est accompagné de **métadonnées** qui le décrivent.
    - On **structure** les **données** pour retrouver facilement des informations et les traiter automatiquement. Une **table** est un ensemble de **données** organisées sous forme de tableau avec en colonnes les **descripteurs** et en lignes les différents **objets** enregistrés dans la **table**.
    - Les opérations de traitement consistent à **filtrer** selon un critère ou une combinaison de critères (OU, ET, NON), **trier** pour réordonner les **objets** dans la **table**, **calculer**...
    - Structurer les **données** sur plusieurs **tables** permet d'éviter les redondances et de ne mettre à jour qu'une seule fois chaque **valeur** en cas de changement.
    - En croisant (**fusionnant**) deux **tables** ayant un **descripteur** commun (une **jointure**), on peut générer des informations nouvelles...




## Notion de binaire

Quelque soit la donnée, un ordinateur ne dispose que des chiffres `0` et `1` pour la représenter numériquement.

### Les nombres entiers

???- tip "Le tour de magie de l'informaticien"

    Choisissez un nombre entier compris entre 1 et 31 ?

    Un informaticien est capable de le retrouver en vous posant cinq questions :

    <center><img src="https://ericecmorlaix.github.io/img/Binaire-TourDeMagie.svg" alt="5 cartes" width=80%></center>

    <!-- <center> Source : <a href="https://culturemath.ens.fr/thematiques/college/tour-de-magie-binaire">Cliquez ici pour trouver une explication, si besoin..."</a></center> -->

    Comment fait-il ?

???- example "L'expérience pour compter comme un ordinateur"

    Pour apprendre à compter comme le font les ordinateurs, vous allez commencer par jouer avec des cartes...

    === "Préparation"

        Disposez les cinq cartes que vous avez reçues sur la table en face de vous en respectant l’ordre ci-dessous  :
        
        <center><img src="https://ericecmorlaix.github.io/img/5_Cartes.svg" alt="5 cartes" width=60%></center>

    === "Phase 1"

        1. Demandez à votre voisin de choisir un entier au hasard (ex :  $6$ , $21$, $15$ …) ;
        2. Retournez ou ne retournez pas certaines cartes de façon à compter autant de points visibles que le nombre entier choisi ;
        3. Maintenant inversez les rôles, et demandez à votre voisin d’afficher un autre entier que vous avez choisi au hasard...

        ***
        === "Question 1"
            Existe-t-il un nombre qui peut être représenté de deux façons différentes avec les cartes ?
        === "Réponse 1"
            
        ***
        === "Question 2"
            Peut-on afficher n'importe quel entier ?
        === "Réponse 2"

        ***
        === "Question 3"
            Quel est le maximum ?
        === "Réponse 3"

        ***

        > *Comptez à partir de $0$ et essayez de repérer le mécanisme de progression...*

    === "Phase 2"

        Pour chaque carte :
        
        - on note **``1``** si elle est tournée du côté visible (recto) ;
        - et on note **``0``** si la face est invisible (côté verso).

        ***
        === "Question 1"
            Quel nombre est représenté par le mot **``01001``** ?
        === "Réponse 1"

        ***
        === "Question 2"
            Quel nombre est représenté par le mot  **``00000``** ? 
        === "Réponse 2"

        ***
        === "Question 3"
            Quel nombre est représenté par le mot  **``11111``** ?
        === "Réponse 3"

        ***
        === "Question 4"
            Comment écrit-on **$17$** en binaire ?  
        === "Réponse 4"

        ***
        > *Etc… entraînez vous avec vos voisins à convertir différents nombres entiers dans le sens décimal => binaire  et  binaire => décimal...*


???- success  "La blague de l'informaticien"

    Vous devriez maintenant être en mesure de comprendre cette affirmation :
    <center><img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIHdpZHRoPSIxMDc2cHgiIGhlaWdodD0iNDE3cHgiIHZpZXdCb3g9Ii0wLjUgLTAuNSAxMDc2IDQxNyI+PGRlZnMvPjxnPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIwMC41LDEzMi41KSI+PHN3aXRjaD48Zm9yZWlnbk9iamVjdCBzdHlsZT0ib3ZlcmZsb3c6dmlzaWJsZTsiIHBvaW50ZXItZXZlbnRzPSJhbGwiIHdpZHRoPSI3MDUiIGhlaWdodD0iMTc4IiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBpbmxpbmUtYmxvY2s7IGZvbnQtc2l6ZTogMTJweDsgZm9udC1mYW1pbHk6IEhlbHZldGljYTsgY29sb3I6IHJnYigwLCAwLCAwKTsgbGluZS1oZWlnaHQ6IDEuMjsgdmVydGljYWwtYWxpZ246IHRvcDsgd2lkdGg6IDcwN3B4OyB3aGl0ZS1zcGFjZTogbm93cmFwOyBvdmVyZmxvdy13cmFwOiBub3JtYWw7IHRleHQtYWxpZ246IGNlbnRlcjsiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OmlubGluZS1ibG9jazt0ZXh0LWFsaWduOmluaGVyaXQ7dGV4dC1kZWNvcmF0aW9uOmluaGVyaXQ7d2hpdGUtc3BhY2U6bm9ybWFsOyI+PHNwYW4gc3R5bGU9ImZvbnQtc2l6ZTogNDhweCI+PGZvbnQgZmFjZT0iQ29taWMgU2FucyBNUyIgc3R5bGU9ImZvbnQtc2l6ZTogNDhweCIgY29sb3I9IiMwMDAwOTkiPklsIHkgYSAxMCBjYXTDqWdvcmllcyBkJ2luZGl2aWR1cyw8YnIgLz5jZXV4IHF1aSBjb21wcmVubmVudCBsZSBiaW5haXJlPGJyIC8+ZXQgbGVzIGF1dHJlcy4uLjwvZm9udD48YnIgLz48L3NwYW4+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9IjM1MyIgeT0iOTUiIGZpbGw9IiMwMDAwMDAiIHRleHQtYW5jaG9yPSJtaWRkbGUiIGZvbnQtc2l6ZT0iMTJweCIgZm9udC1mYW1pbHk9IkhlbHZldGljYSI+Jmx0O3NwYW4gc3R5bGU9ImZvbnQtc2l6ZTogNDhweCImZ3Q7Jmx0O2ZvbnQgZmFjZT0iQ29taWMgU2FucyBNUyIgc3R5bGU9ImZvbnQtc2l6ZTogNDhweCIgY29sb3I9IiMwMDAwOTkiJmd0O0lsIHkgYSAxMCBjYXTDqWdvcmllcyBkJ2luZGl2aWR1cywmbHQ7YnImZ3Q7Y2V1eCBxdWkgY29tcHJlbm5lbnQgbGUgYmluYWlyZSZsdDticiZndDtldCBsZXMgYXV0cmVzLi4uJmx0Oy9mb250Jmd0OyZsdDticiZndDsmbHQ7L3NwYW4mZ3Q7PC90ZXh0Pjwvc3dpdGNoPjwvZz48cGF0aCBkPSJNIDI2OS41IDEwNC41IEMgNTUuNSAxMDQuNSAyIDIwNyAxNzMuMiAyMjcuNSBDIDIgMjcyLjYgMTk0LjYgMzcxIDMzMy43IDMzMCBDIDQzMCA0MTIgNzUxIDQxMiA4NTggMzMwIEMgMTA3MiAzMzAgMTA3MiAyNDggOTM4LjI1IDIwNyBDIDEwNzIgMTI1IDg1OCA0MyA2NzAuNzUgODQgQyA1MzcgMjIuNSAzMjMgMjIuNSAyNjkuNSAxMDQuNSBaIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS13aWR0aD0iNCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyLDMpIiBvcGFjaXR5PSIwLjI1Ii8+PHBhdGggZD0iTSAyNjkuNSAxMDQuNSBDIDU1LjUgMTA0LjUgMiAyMDcgMTczLjIgMjI3LjUgQyAyIDI3Mi42IDE5NC42IDM3MSAzMzMuNyAzMzAgQyA0MzAgNDEyIDc1MSA0MTIgODU4IDMzMCBDIDEwNzIgMzMwIDEwNzIgMjQ4IDkzOC4yNSAyMDcgQyAxMDcyIDEyNSA4NTggNDMgNjcwLjc1IDg0IEMgNTM3IDIyLjUgMzIzIDIyLjUgMjY5LjUgMTA0LjUgWiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjN2YwMGZmIiBzdHJva2Utd2lkdGg9IjQiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9Im5vbmUiLz48L2c+PC9zdmc+" width=60% /></center>

    <center><a href="https://www.lemonde.fr/blog/binaire/2014/02/10/les-blagues-sur-linformatique-episode-1/">Cliquez ici si vous avez encore besoin d'explications pour comprendre cette blague..."</a></center>

### Les textes

???- abstract "Le codage des caractères alphanumériques"

    Chaque caractère alphanumérique présent dans nos données textuelles est codé pour être représenté par un nombre binaire.

    Voici la table [ASCII](https://fr.wikipedia.org/wiki/American_Standard_Code_for_Information_Interchange) (American Standard Code for Information Interchange)

    ![image ascii.png](../images/ascii.png){.center }

    Le mot «OK» sera donc codé en binaire par `01001111 01001011`.

???- example "Exercice :"
    === "Question"
        En vous répartissant le travail, décodez la phrase (codée en décimal) :
        `83|78|84|44|32|99|39|101|115|116|32|116|111|112|32|33`
    === "Réponse"

