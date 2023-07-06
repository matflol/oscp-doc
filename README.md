# Préparation à l'examen OSCP

## Guide d'examen

https://help.offsec.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide

- Il est recommandé de devenir le plus familier possible avec le guide d'examen officiel, voir l'apprendre presque par cœur, AVANT d'être rendu à faire l'examen.

- Il est facile d'échouer l'examen même si on a trouvé tous les « flags », car une certaine consigne ou exigence n'a pas été respectée. 

- Il peut être bénéfique, pendant la pratique et la préparation, de déjà s'habituer à adopter les règles entourant l'examen. Comme cela, les réflexes commencent à s'encrer dans notre tête, et ça devient automatique lorsqu'on est rendu en situation d'examen et de rapport final. 

- Cela s'applique particulièrement pour ces points:
	- Prise de notes et documentation : développez votre méthode avant l'examen. Pensez à ce que vous aurez besoin d'inclure dans votre rapport, pour vous assurer de prendre les notes correspondantes pendant que vous travaillez sur les machines. C'est désagréable de devoir aller recompromettre des machines pour aller prendre des screenshots oubliés; 
	- Inclure les preuves de code d'exploit et de « flags » comme OffSec le veut dans son rapport pour que ça devienne automatique;
	- Outils restreints : ne développez pas une méthodologie reposant sur des outils interdits à l'examen;
	- Restrictions Metasploit : toujours avoir en tête les restrictions entourant son utilisation, il ne faut pas penser que c'est interdit de s'en servir, mais il faut s'en servir dans les barèmes. À noter que `msfvenom` et `multi/handler` sont free-for-all.

## Points bonus

Il est possible d'aller se chercher 10 points bonus pour l'examen en remplissant les critères définis par OffSec. Ces critères sont, au moment de l'écriture:
- Avoir soumis au moins 80% de bonnes réponses dans les exercices de tous les sujets du matériel de cours en ligne, ET;
- Avoir soumis au moins 30 « flags » trouvés sur les machines des différents laboratoires fournit par OffSec. 
- Vérifier les critères officiels publiés par OffSec en cas de changement depuis l'écriture de ce guide.

## Exercices 

- OffSec a un serveur Discord très actif avec une communauté assez vivante. Si vous bloquez sur un point, c'est certain que quelqu'un d'autre a déjà posé la même question sur Discord. 

- Aussi, des « student mentors » d'OffSec sont constamment sur Discord et peuvent répondre à vos questions.

- OffSec a implanté un système automatisé de « hints » pour certains exercices et labs, si vous bloquez complètement sur certaines étapes, vous pouvoir recevoir un petit « hint » via Discord sans même avoir à parler avec quelqu'un.

## Laboratoires

OffSec a implanté un nouveau système de laboratoires en 2023 et c'est beaucoup mieux que c'était par le passé. Il y a au fond deux styles de laboratoires différents:

### Les « challenges » (Medtech, Relia, Skylark)

- Ce sont des environnements corporatifs simulés contenant un ensemble de machines sur différents sous-réseaux. Certaines machines ont des liens entre elles, et d'autres non. C'est très similaire à un « Pro Lab » d'Hack The Box. 

- À mesure que des machines sont compromises, on ramasse graduellement des éléments qui nous permettent d'avancer vers d'autres machines jusqu'à compromission complète du lab.

- Ils sont classés en ordre de difficulté :
	- Medtech: Facile
	- Relia: Moyen
	- Skylark: Difficile

- Les « challenges » sont amusants et bénéfiques pour l'apprentissage et la pratique, nous font voir toutes sortes de techniques et apprendre toutes sortes de choses courantes et parfois obscures aussi, mais il faut comprendre qu'ils ne sont PAS directement une pratique pour l'examen. Le format des « challenges » a très peu de similitudes avec l'examen OSCP. Plusieurs choses rencontrées dans les « challenges » ne seront jamais vus dans l'examen OSCP. 

- Les « challenges » peuvent être considérés comme du contenu supplémentaire pour aller un peu plus loin. Cela s'avère particulièrement vrai pour « Skylark » qui contient des choses parfois très obscures, qui ne sont parfois pas dans le contenu du cours.

- Si le temps de préparation est un enjeu, il peut être bénéfique de prioriser les 3 répliques d'examen avant les « challenges ». Plusieurs personnes vont d'ailleurs faire de fond en comble les 3 répliques d'examens en premier, et seulement revenir aux « challenges » s'il leur reste du temps. 

- Pour les « challenges », comme ça nous fait aller plus loin, et qu'il y a beaucoup de machines et d'indices à trouver, il est recommandé de ne pas être trop sévère envers soi-même avec les restrictions d'outils et de temps. Après tout, l'examen ne ressemblera pas à cela du tout, donc ce n'est pas réaliste de tenter de le terminer en 24h. Idem si on rencontre des défis qui se font beaucoup plus facilement avec Metasploit. 

### Les répliques d'examen (OSCP A, B, C)

- C'est un nouveau format de lab ajouté par OffSec qui réplique fidèlement les paramètres utilisés dans les examens OSCP. Pour valider si on est prêt ou pas à aller passer l'examen, c'est le meilleur barème. 

- Il n'y a pas vraiment de différence de difficulté entre A, B, et C. Il faut le voir comme 3 instances possibles différentes de ce que pourrait avoir l'air un examen. Certaines machines peuvent être très simples, et parfois d'autres un peu moins, mais la difficulté est globalement similaire entre les différentes répliques.  

- Le format de chaque réplique d'examen est fidèle à ce qu'on rencontre dans l'examen OSCP:
	- 3 machines dans une domaine AD: 2 machines membres, 1 machine DC. Les machines membres ont 2 « flags » (local.txt pour un user lowpriv, proof.txt pour local admin), et le DC a un seul flag proof.txt (généralement on atteint un Domain admin). 
	- 3 machines « standalones » avec absolument aucun lien entre elles ou avec l'AD. Chaque machine a un local.txt pour un user lowpriv, et un proof.txt pour root ou local admin. 
	- Il n'y a plus de « buffer overflow », tout comme dans l'examen dorénavant, depuis le lancement de la version 2023 du cours.

- Il peut être bénéfique en faisant les répliques d'examen de simuler être en situation réelle d'examen. Cela aide à se mettre dans l'état d'esprit qui sera nécessaire à avoir durant l'examen, voici quelques examples:
	- Se chronométrer. Il n'y a pas de problème à mettre en pause le chronomètre lorsqu'on arrête de travailler sur le lab. Même si on ne fait pas le lab en 24h consécutives, ça peut quand même être intéressant de savoir combien d'heures totales on a mises sur la pratique, pour commencer à estimer si on sera capable de le faire en 23h45 en situation réelle d'examen;
	- Respecter les restrictions d'outils et de documentation: ça aidera beaucoup si on a déjà les bons réflexes, au lieu d'essayer de casser des mauvais réflexes à l'examen;
	- Rapport: il est recommandé de simuler la production d'un rapport au moins 1 fois avant l'examen. En situation réelle d'examen, vous serez stressé et pressé dans le temps, ce n'est pas le temps d'essayer de trouver une nouvelle façon de créer un rapport. Cela devrait être déjà acquis.
	- Je recommande de faire un rapport complet de bout-en-bout pour au moins 1 des 3 pratiques d'examen pour peaufiner votre processus de production de rapport et corriger tout problème. Ce n'est pas agréable de réaliser à la dernière minute qu'on a un problème de génération de rapport (fait vécu).
	- Indices: il ne faut pas se sentir trop mal d'avoir besoin d'un indice de temps à autre. Cela reste une pratique. L'important est de noter et assimiler le pourquoi a on été bloqué, afin d'éviter un blocage similaire à l'examen. Cela peut être une belle opportunité d'ajouter des vérifications, techniques ou outils à nos notes et méthodologie. 

## Rapport 

OffSec n'est pas très précis dans son guide d'examen sur ce qui compte ou ne compte pas dans le rapport. Il semble que les points sont attribués purement selon les machines réussies, et ensuite ça passe ou ça casse selon la recevabilité du rapport.

Il y a des attentes précises seulement pour:
- Le code d'exploit, on peut seulement mettre un lien vers l'exploit utilisé si on ne l'a pas modifié, mais si on l'a modifié on doit montrer les changements faits et expliquer pourquoi.
- Les preuves, ou « flags »: pour chaque flag on doit montrer son contenu dans un vrai shell interactif, accompagné de l'adresse IP de la machine. Un "web shell" ne suffit pas, les points ne seront pas accordés dans ce cas. 

### Gabarit OffSec

Certains font leur propre rapport personnel et ça passe, mais une recette prudente est de se limiter au gabarit officiel fournit par OffSec. Comme cela, on est sur de remplir les attentes. Ils fournissent un gabarit en format Office sur la page du guide d'examen. Il suffit de remplir les trous avec le contenu de notre examen.

https://www.offensive-security.com/pwk-online/OSCP-Exam-Report.docx<br>
https://www.offensive-security.com/pwk-online/OSCP-Exam-Report.odt

La majorité des étudiants semblent suivre cette solution et s'en sortent bien. Personnellement, j'ai eu énormément de difficulté à ramener mes notes d'Obsidian vers MS Word, ça cassait constamment la mise en page du rapport, et je perdais énormément de temps à essayer de réparer la mise en page au lieu d'avancer mon rapport. J'ai donc regardé pour une autre façon de faire. 

### Script Linux

Si travailler dans un document Office n'est pas efficace pour vous, il existe d'autres solutions comme celle-ci faite par un membre de la communauté : 

https://github.com/noraj/OSCP-Exam-Report-Template-Markdown

Voici un résumé de cette solution:
- Ce bon samaritain travaillait uniquement sous Linux et avait l'habitude de générer ses notes en « Markdown », et a donc converti le rapport officiel d'OffSec en format « Markdown ». 
- Il a ensuite créé un script Ruby qui utilise « pandoc » et « LaTeX » pour convertir le rapport depuis le format « Markdown » vers un beau fichier PDF bien présenté. 
- Le PDF généré respecte toutes les exigences actuelles d'OffSec: inclure notre « OS ID », nommer le fichier avec une nomenclature précise, le placer dans une archive 7zip du même nom, etc. 
- On a plusieurs choix de couleurs et de formatage pour les « code blocks ». 

C'est une excellente solution et puisque mes notes sont exclusivement en « Markdown », c'était une vraie joie de passer mon rapport directement d'Obsidian vers un PDF présentable sans jouer dans Microsoft Office. Par contre, garder en tête ces bémols:
- Au fil des mois, si OffSec sort un nouveau template de rapport, ça ne veut pas dire que le bon samaritain va automatiquement le convertir et l'intégrer à son projet. Il vaut mieux vérifier au moment de faire son examen. Au besoin, ce n'est pas très compliqué d'aller chercher le dernier rapport OffSec et le mettre en « Markdown » pour servir de gabarit.
- Si OffSec modifie ses exigences et critères pour le rapport, ça ne veut pas dire que le bon samaritain va modifier son projet automatiquement. Il vaut mieux vérifier aussi avant de l'utiliser. 
- Il est recommandé de tester la solution de bout-en-bout au moins une fois. J'avais personnellement testé l'outil rapidement et la génération fonctionnait très bien, mais une fois en situation d'examen, j'ai transféré mes notes Obsidian de mon hôte vers ma VM, généré le rapport, et mes copies d'écran étaient brisées. Je n'avais pas assez testé le processus. Il semble que le problème n'était pas l'outil en soit mais ma façon d'insérer les copies d'écran dans Obsidian. Ça causait un problème avec « pandoc ». J'aurais du mieux tester le processus de bout-en-bout au préalable à tête reposée.

# Examen

## Conditions d'examen

Évidemment, se rapporter au guide d'examen officiel pour avoir la dernière version à jour, mais voici un résumé: 

- L'examen est « proctored », donc surveillé à distance en tout temps via webcam. Il faut donc prévoir le coup et avoir une pièce calme où on peut éviter d'être dérangé. Si le surveillant voit d'autres personnes dans la pièce, vous mettez à risque votre examen.
- Quand on part en pause, on fait juste avertir le surveillant et on peut se lever et partir. **Le temps continue de tourner.** On peut fermer la cam pendant ce temps. On peut se déconnecter, mais j'ai trouvé plus efficace de laisser toutes mes choses ouvertes pour resauter directement dans l'examen à mon retour. 
- Il vous sera demandé de prendre votre caméra **avec le même appareil** et filmer les environs et de démontrer qu'il n'y a aucun autre dispositif électronique dans la pièce: autres ordinateurs, télés, téléphones, etc. Si cela demande d'adapter votre pièce, pensez-y avant le jour J. 
- Le logiciel de surveillance supporte plusieurs écrans, mais ne semble pas aimer les écrans en mode portrait. J'ai du basculer mon second écran en mode paysage pour être capable de présenter mes deux écrans au surveillant.
- On dispose de 23:45h pour faire l'examen. 
- On reçoit un « VPN Pack » similaire à ce qui est utilisé pour les laboratoires. **Les « flags » doivent absolument être soumis dans un portail web accessible depuis le VPN.**
- Une autre plage de temps séparée nous est allouée pour la production du rapport.

## Pointage

Au moment d'écrire ces lignes, le pointage de l'examen fonctionnait comme suit:
- Il faut accumuler 70 points pour réussir l'examen. Maximum 100 points.
- L'ensemble de 3 machines dans un domaine AD vaut 40 points ou 0 points. Il faut compromettre l'ensemble des machines pour avoir les 40 points, sinon c'est 0.
- Les 3 machines « standalone » donnent 10 points pour obtenir un shell lowpriv, et 10 autres points pour obtenir un shell root/admin, donc 20 points potentiels chacune.

Dépendamment des points bonis, cela crée donc quelques scénarios possibles pour obtenir la note de passage:
- 10 points bonis + AD set 40 points + 1 machine « standalone » complétée = 70 points
- 10 points bonis + 3 machines « standalones » complétées = 70 points
- AD set 40 points + 2 machines « standalones » complétées = 80 points
- Sans les points bonis, vous êtes donc obligés de réussir le set d'AD, puisque 60 points des 3 « standalones » ne seraient pas suffisants. 

Ne pas oublier que pour prouver la réussite des machines, il faut:
- Soumettre toutes les preuves « local.txt » et « proof.txt » dans le portail web;
- Inclure toute la documentation nécessaire dans le rapport démontrant la compromission des machines, en suivant les exigences d'OffSec.

# Post-examen (rapport)

- Dès que le temps est écoulé pour l'examen, une nouvelle période de 24h commence qui représente le temps restant pour soumettre notre rapport. 
- OffSec a un portail web où déposer le rapport. Il y a des requis spécifiques à suivre qui sont détaillées dans le guide d'examen, particulièrement pour le nom du fichier du rapport et son format. 
- OffSec affiche un délai maximal de 10 jours pour revenir avec les résultats par courriel. On peut aussi potentiellement voir son résultat un peu plus rapidement dans le portail web OffSec (onglet EXAM).
