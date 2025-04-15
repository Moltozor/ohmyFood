commande sass: sass style.scss style.css --watch


Animation css:

Il existe deux moyens de créer des animations en CSS : les transitions, et les keyframes.

Propriété: transform -> une seul propriété transform par élément
fonction: scale() -> permet de modifier la taille d’un élément

exemple:

&:hover {
    transform: scale(valeur);
}

---------------
Chapitre: TRANSITION

transition: -> À ajouter dans le selecteur et non dans le :hover (pseudoclasse)

transition-property: transform; -> déclare une transition dans le selecteur (IMPORTANT)

transition-duration: permet d'indiquer la durée que prendra votre transition (secondes, millisecondes)

transition-delay: -> retarde le début d'une animation - la valeur de  transition-delay  peut également être définie directement dans la propriété transition
            FONCTION DE TIMING LINEAIR

transition-timing-function: ->  règle la courbe d’accélération d’une transition.
transition-timing-function: linear;
ease-in-out

            fonction cubic-bezier
cubic-bezier(x1, y1, x2, y2) coordonnées de la fonction cubic pour gérée l'accélération et la décélération.
à
Combiner les syntaxes (factoriser) : (transition-property: transform + transition-duration ) = transition: transoform 1s;
transition: background-color 1s;

Déclencher une transition avec une pseudoclasse:

pseudoclasses courament utilisées: :hover, :active, :focus, :valid, :invalid, :not(), :checked, :enabled, :disabled

Modifiez les éléments voisins avec les pseudoclasses

exemple:

.selecteur_btn {
    propriétés....

    &:hover + .selecteur_voisin {
        propriétés...
    }
}

.selecteur_voisin {}

