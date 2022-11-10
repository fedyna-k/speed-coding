# Speed Coding #1

## Premier challenge

Les membres du club wes veulent faire une estimation du nombre de sessions ski qu'ils peuvent faire en une année.

Pour se faire, ils ont decidé de chercher le bulletin météo historique des $n$ dernières années pour savoir quand il commence généralement à neiger. Pour chaqu'une des $n$ dernières années ils relèvent $d_i$ le nombre de jours entre la fin de l'été et le premier jour de neige de l'$i$ème année.

Compte tenu des données historiques. Les membres veulent savoir le nombre d'années consécutives juste avant l'année en cours avec un plus grand écart entre la fin de l'été et le premier jour de neige. Plus formellement, supposons que l'année en cours soit $m$. Ensuite, il aimeraient déterminer le plus grand entier $k$ pour lequel $d_{m-1},d_{m-2},...,d_{m-k}>d_m$, ou déterminer qu'il n'avait jamais neigé aussi tôt au cours des dernières $m$ années.

### Input :

La première ligne de l'entrée contient deux entiers $n$ et $d_m$. It is guaranteed that $1 \le n \le 100$ and $0 \le d_m \le 100$ .
La ligne suivante de l'entrée contient $n$ nombres entiers.le ième entier indique $d_{m-i}$ avec $0 \le d_{m-i} \le 100$.

### Output : 

S'il existe un entier $k$ pour lequel $d_{m-k} \le d_m$, print "Il n'avait pas neigé aussi tôt depuis $k$ années !" . Sinon, écrivez "Il n'avait jamais neigé aussi tôt!" .

### Exemples :
#### input :
>4 2 <br>
>3 3 3 2

#### output : 
>Il n'avait pas neigé aussi tôt depuis 3 années !"

## Deuxième challenge

Vous êtes au sommet d'une piste noire, le vent traverse vos cheveux alors que vous vous apprétez à vivre la descente de votre vie.

C'est alors que vous vous lancez sur la poudreuse, tout se passe bien, quand tout à coup : le drame.

Vous ne sentez plus que de la glace sous vos pieds, les skis dérapent et vous partez en hors piste.

L'hors piste est un endroit assez dangereux dans lequel il y a beaucoup d'arbres. Heureusement, vous avez suivi un entraînement avec Stalone et les arbres ne font que vous ralentir.

En supposant que vous glissez en ligne droite, nous cherchons à savoir quelle trajectoire permet de moins vous ralentir (i.e. : Celle qui vous fait rencontrer le moins d'arbres).

Dans la forêt, tout se ressemble, c'est pourquoi les arbres (repérés par des ``#``) se répètent suivant un pattern défini.

Prenons cette portion de forêt :
```
...#..#...#...#
.##...#..#.#..#
#..##..#...##..
.#...#....##..#
#....#...#.#...
..#...#..#..#..
.....#........#
.......#.......
```

Cette portion s'étend alors vers la droite de la façon suivante :
```
...#..#...#...# > ...#..#...#...#...#..#...#...#
.##...#..#.#..# > .##...#..#.#..#.##...#..#.#..#
#..##..#...##.. > #..##..#...##..#..##..#...##..
.#...#....##..# > .#...#....##..#.#...#....##..#
#....#...#.#... > #....#...#.#...#....#...#.#...
..#...#..#..#.. > ..#...#..#..#....#...#..#..#..
.....#........# > .....#........#.....#........#
.......#....... > .......#..............#.......
```

En commençant en haut à gauche sur la pente, déterminez le nombre d'arbres rencontrés pour des pas de :
- 1 à droite, 1 en bas
- 3 à droite, 1 en bas
- 5 à droite, 1 en bas
- 7 à droite, 1 en bas
- 1 à droite, 2 en bas

**Quel est la valeur du produit de chaque nombre d'arbres rencontrés pour les différents pas ?**