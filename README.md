# Frises de l'histoire de la gauche

Infographie interactive en deux pages, sur fond noir, inspirée de la maquette Figma « Hist gauche ».

- **`index.html` · Histoire de la gauche** : les grands courants de la gauche française de 1789 à 2026, avec leurs scissions (radicaux, anarchistes, socialistes, communistes, trotskistes, maoïstes, écologistes, gauche radicale) et leurs ralliements.
- **`mouvements-sociaux.html` · Mouvements sociaux** : les mouvements sociaux en France du Moyen Âge (1358) à aujourd'hui, une colonne par année.

## Fonctionnement

- Seule la première bulle est visible au chargement ; un clic affiche son texte et fait apparaître la suite.
- Bouton « Détail » : ouvre une fenêtre à droite avec la date, l'intitulé et le texte détaillé.
- Navigation : barre de défilement, flèches, molette ; zoom avec les boutons − / +, Ctrl + molette ou les touches + / − / 0.

Aucune dépendance à installer : ouvrez simplement `index.html` dans un navigateur. Les images des bulles sont intégrées directement dans la page.

## Modifier la frise

Chaque bulle est un bloc `<div class="step">` :

| Attribut | Rôle |
|---|---|
| `data-id` | identifiant unique de la bulle |
| `data-next` | bulles suivantes (plusieurs ids = scission, vide = fin de branche) |
| `data-branch` | nom affiché au départ d'une branche |
| `data-track` | ligne de la branche (0 = ligne principale, négatif = au-dessus) |
| `data-chapter` | titre de chapitre affiché à partir de cette bulle |
| `data-shift` | décale la bulle et la suite de la frise vers la droite (px) |
| `data-text` | `above` / `below` : position du texte |
| `style="--img: url(...)"` | image de fond de la bulle |

Les textes des bulles sont pour l'instant des textes provisoires (lorem ipsum).
