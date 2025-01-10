# Project-M1-MPE

Notre projet vise à répondre à une question que beaucoup de Français se posent : quel café me correspond le plus ?

Afin de pouvoir utiliser notre programme, il faut tout d’abord télécharger le script R fourni et avoir accès à la base de données. Cette base de données doit être téléchargée sur RStudio. Vous devez également vous assurer que le package readxl est bien installé.

Pour répondre à la question posée, nous avons donc développé un programme qui interagit avec l’utilisateur en lui posant toute une série de questions basées sur les caractéristiques de chacun des cafés. L’idée principale de notre projet est qu’à partir des réponses de l’utilisateur aux 8 questions, le programme lui propose le café qui lui correspond le plus parmi un total de 30 options. 

Nos critères sont les suivants :

Le taux de caféine : l’utilisateur a le choix moyennement intense en caféine, fort en caféine ou intense en caféine
La taille du café : 3 tailles sont proposées à l’utilisateur concernant le café qu’il souhaite : petit, moyen ou grand
La saison : l’utilisateur choisit s’il souhaite boire son café en été, automne ou hiver, ou bien s’il souhaite un café adapté à toutes les saisons
Température : l’utilisateur peut indiquer s’il préfère un café plutôt froid, chaud ou bien s’il est indifférent entre les deux
Goût : nous avons ici fait le choix de distinguer les cafés amer et sucrés
Quantité de lait : l’utilisateur a la possibilité de choisir s’il souhaite un café sans lait, avec peu de lait ou bien beaucoup
Budget : plusieurs prix sont proposés, l’utilisateur sélectionne celui qui lui convient le plus
Objectif : enfin, l’individu indique ce qu’il attend de son café. Il a donc le choix entre “Découverte” s’il souhaite simplement un café qui change un peu de son quotidien, “Productivité” s’il souhaite un café qui lui donne de l’énergie ou “Détente et social” si son objectif est simplement de se poser avec des amis autour d’un bon café.

Lors de la création de ce projet, nous avons renommé nos colonnes pour plus de lisibilité et nous avons créé une première fonction qui permet de poser des questions à l’utilisateur avec des choix de réponses prédéfinis, que nous avons ensuite classé dans l’ordre que nous souhaitions pour davantage de cohérence.

Nous entrons ensuite dans notre fonction principale. Dans un premier temps, les questions sont posées à l’individu concernant la taille du café qu’il souhaite, sa température, son objectif de consommation… Un point important concerne les tailles choisies. Par exemple, nous avons fait en sorte que lorsqu’il indique souhaiter un café “petit”, alors dans notre base de données sont pris en compte les cafés disponibles uniquement en taille “Petit” mais également ceux disponibles en “Petit, Moyen” et “Petit, Moyen, Grand”. A partir des 8 réponses de l'utilisateur, 8 vecteurs sont créés et stockent les cafés qui correspondent aux réponses de l’individu concernant chacun des critères. Nous avons ensuite combiné ces vecteurs en un seul, ce qui nous montre la fréquence d’apparition de chacun des cafés. Les trois cafés avec la fréquence d’apparition la plus élevée sont présentés à l’utilisateur ainsi que le meilleur, affiché avec son goût et le lien pour le commander.

Dans un second temps, nous demandons à l’utilisateur les deux critères parmi les 8 qu’il veut absolution que le café qui lui soit proposé respecte. Nous vérifions également que les deux critères sélectionnés sont distincts. Si c’est le cas, le café qui lui est proposé reste le même que précédemment. Si ce n'est pas le cas, on lui redonne un nouveau café qui semble plus adapté pour lui et qui respecte les critères qu’il souhaite. A nouveau le programme lui affiche le lien pour qu’il puisse le commander.

Pour finir, il est possible d’améliorer notre code. En effet, il est tout à fait possible d’intégrer davantage de critères de choix tels que le pays d’origine des grains de café ou encore sa méthode de préparation. Par ailleurs, une bonne idée pourrait être de pondérer les préférences de l’utilisateur, ce qui nous permettrait d’obtenir son ordre de préférences concernant les critères de choix. Enfin, il peut être interessant de réaliser des représentations graphiques qui représentent la compatibilité des différents cafés. 
