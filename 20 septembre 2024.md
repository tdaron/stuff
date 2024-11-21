#cm 
Théorie des graphes
Devoirs: 5pts de l'exam
Train
[     ]-[     ]-[    ]-[     ]-[     ]

## Graphes connexes, eulériens et bipartis

Un parcours est une suite $v_0 e_1 v_1 e_2 \ldots e_n v_n$, où $v_1, v_2, \ldots$ sont des sommets, et $e_1, e_2, \ldots$ sont des arêtes. La longueur du parcours est son nombre d'arêtes $n$. Le sommet d'origine est $v_0$, le sommet de destination $v_n$. Les autres sommets sont dits intérieurs. Un parcours est fermé si $v_0=v_n$.

Un chemin est un parcours dont les sommets et arêtes sont tous distincts.

Un cycle est un chemin fermé.
Un graphe est connexe si pour chaque paire de points il existe un parcours qui les relie.

Les composantes connexes d'un graphe sont ses sous-graphes connexes maximaux.

Un parcours est eulérien s'il visite chaque arête une et une seule fois. Un graphe est eulérien s'il existe un parcours eulérien fermé.

eulérien -> Un parcours existe passant 1 fois par toutes les arrêtes en revenant au départ

Eulérien => degré pairs: Preuve "facile" faite par Euler

Degré pairs => Eulérien: Plus complexe, "comment fabriquer un parcours eulérien"

On part d'un noeud et on fait un parcours aléatoire. Une fois qu'on est bloqués, on peut repartir d'un autre noeud du graphe qu'on a parcouru qui a une arrête voisine toujours libre afin de faire un deuxième parcours, et on peut montrer qu'on pourra relier les deux facilement.

Preuve (a renoter car pas convaincu de ma façon de l'écrire):

Quand je parle de parcours je parle de parcours *eulérien fermé* ici.

On part d'un nœud arbitraire *u*.
On construit un parcours partant de *u* sans jamais emprunter 2 fois la même arrête.
$\forall$noeud visité != u on peut toujours continuer le parcours car nombre d'arrêtes déjà "visitées = 2 fois passages précédents +1" (si on est déjà passé 2 fois par le noeud on a brûlé 4 arrêtes, et si on revient sur le noeud ça fait 5, il doit exister une 6 ème par parité) car par parité du degré, il existe une arrête *libre*. On est bloqué seulement en u -> parcours fermé. Si il visite tout le graphe OK stop. Si il $\exists$ une arrête non visitée, alors il existe un parcours incident au parcours des arêtes déjà visitées par connexité. L'idée est que le noeud *p* dont partira ce "nouveau cycle", étant connecté au parcours initial permettra de switcher. On fera:

*u* -> *p* puis a p on diverge sur le chemin de *p*, et une fois revenus a *p* on repart sur la boucle initial de *u*. 

Par contre comment est ce qu'on sait que le graphe des arrêtes non visitées est connexe.. 

**Théorème**: Un graphe connexe possède un parcours eulérien (pas fermé) ssi le nombre de noeuds de degré impair est zéro ou deux

**Théorème**: 




