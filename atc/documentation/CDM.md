---
title: Collaborative Decision Making
description: 
published: true
date: 2026-07-19T19:36:08.056Z
tags: 
editor: markdown
dateCreated: 2026-02-28T22:39:29.636Z
---

![banner_tools_fr.png](/banners/banner_tools_fr.png)

# Introduction 
Le CDM (Collaborative Decision Making) est un projet européen visant à améliorer la fluidité de la plateforme le long du processus de départ. Il permet d'améliorer le fonctionnement de la plateforme en situation nominale et notamment en cas de demande supérieure à la capacité et, sur VATSIM de faciliter l’application des mesures ECFMP (European Collaboration & Flow Management Project).

## Conditions d’utilisation du CDM

Le CDM est par défaut utilisé sur les plateformes suivantes : LFPG, LFPO, LFMN, LFLL, LFBO et LFML. Toute utilisation en dehors des plateformes précitées n’est pas permise. Avant d’ouvrir ces plateformes, il est <u>recommandé d’avoir une bonne compréhension de ce document</u>.

L’utilisation du CDM est restreinte aux positions de la vigie. Si vous êtes à l’aise avec l’outil et que la charge est compatible, vous pouvez l’utiliser seul (dans le cas où vous seriez seul à la vigie).

Pour fonctionner, le CDM nécessite que <u>l’ensemble des contrôleurs vigie en présence l’utilisent</u> et donc, doivent être familiers avec son fonctionnement.

<u>Note</u> : L’utilisation du CDM n’est pas évaluée dans le cadre d’un CPT.

# GLD (Gestion locale des Départs)
La gestion locale des départs est la composante principale du CDM.
Elle se base sur le partage des informations entre les différents acteurs et calcule une séquence de Départs Blocs permettant de fluidifier le trafic au départ en optimisant l’utilisation des capacités pistes.

Ses gains sont à la fois économiques et environnementaux car elle permet de réduire le temps de roulage en maîtrisant le temps d’attente au seuil de piste.

La GLD est un système qui calcule en permanence pour chaque avion au départ son heure de mise en route, en fonction de toutes les données externes au vol : 
- Les autres avions au départ
- L’exploitant de l'aéroport : capacité de piste
- Les contraintes en vol : regulations / créneaux
- La fluidité du trafic : pression piste contrôlée

# Les horaires clés (Milestones)
Afin d’entrer dans la séquence de départ, tous les trafics doivent envoyer un plan de vol.
Celui-ci contient une EOBT (Estimated Off Block Time), c’est l’heure de repoussage ou de début du roulage sur les stands autonomes.

![stup-list.png](/doc-atc/stup-list.png)

## La TOBT
La Target Off Block Time est l’heure cible que se fixe le trafic comme heure de départ bloc (push-back prêt / avion prêt à rouler dès autorisation). Il est demandé aux trafics d’envoyer une heure estimée de départ et de la mettre à jour afin d’optimiser la séquence de départ.

La confirmation de la TOBT joue un rôle crucial dans le séquencement de départ car une TOBT non confirmée indique que la TSAT n’est plus optimisée dans la séquence après 5 minutes d’inactivité.

Dans EuroScope, cette valeur peut avoir différentes couleurs en fonction de son état : 

|Status|Couleur|
|:-|:-:|
|TOBT non confirmée sans retard au bloc|<span style="color:yellowgreen">VERT CLAIR</span>|
|TOBT confirmée sans retard au bloc|<span style="color:green">VERT</span>|
|TOBT non confirmée avec retard au bloc|<span style="color:yellow">JAUNE CLAIR</span>|
|TOBT confirmée avec retard au bloc|<span style="color:gold">JAUNE</span>|
|TOBT dans + d’une heure ou expirée|<span style="color:orange">ORANGE</span>|

> Il est toujours demandé aux trafics d’envoyer une TOBT afin de la confirmer même si celle-ci correspond à l’EOBT du plan de vol.
{.is-warning}

## La TSAT
La Target Start-Up Approval Time est l’heure de départ bloc séquencée, calculée par la GLD en fonction de différents critères (pression piste, CTOT, TOBT…) à laquelle un avion peut s’attendre à être autorisé à quitter le bloc (mise en route et repoussage) par l’ATC.

En pratique, le trafic est envoyé au sol si il est prêt (il est demandé aux pilotes d'être prêt à TOBT - 10 minutes afin d’assurer la fluidité des départs) et que sa TSAT est valide.

**La fenêtre de validité de la TSAT est de <u>+/- 5 minutes</u>.**

Si la TSAT expire, le pilote doit envoyer ou confirmer une nouvelle TOBT afin d'être reséquencé.

|Status|Couleur|
|:-|:-:|
|TSAT future pas encore valide|<span style="color:yellowgreen">VERT CLAIR</span>|
|TSAT valide (TSAT +/- 5 minutes)|<span style="color:green">VERT</span>|
|TSAT Expirée|<span style="color:orange">ORANGE</span>|
|TSAT future pas encore valide liée à un créneau (CTOT)|<span style="color:royalblue">BLEU CLAIR</span>|
|TSAT valide liée à un créneau (CTOT)|<span style="color:blue">BLEU</span>|
|TSAT Expirée liée à un créneau (CTOT)|<span style="color:red">ROUGE</span>|

Idéalement la TSAT (Target Start-Up Approval Time) ou heure de départ bloc séquencé est la même que la TOBT. Dans le cas ou un retard de + de 5 minutes est nécessaire, on parle de retard au bloc ou startup delay.

## La TTOT

La Target Takeoff Time est l’heure de décollage calculée par le CDM sur laquelle se base la GLD pour ne pas dépasser la capacité de la piste et éviter la congestion des points d'attente. Cette heure est une référence qui n’est pas à respecter absolument, il suffit que le décollage s’effectue avant ou dans le bloc de la TTOT.

Dans la startup list la TTOT peut avoir 2 couleurs, elle est <span style="color:green">VERTE</span> lorsqu’elle est dans le future ou dans le bloc actuel. La TTOT devient <span style="color:orange">ORANGE</span> lors de la fin du bloc auquel elle appartient.
Plusieurs TTOT <span style="color:orange">ORANGES</span> indiquent que le taux de départ actuel est inférieur au taux calculé ou que les valeurs de configuration ne sont pas optimales. 

|Status|Couleur|
|:-|:-:|
|TTOT "Valide"|<span style="color:green">VERT</span>|
|TTOT "Expirée"|<span style="color:orange">ORANGE</span>|

Dans cet exemple, il est entre 1550Z et 1600Z.
![stup-list.png](/doc-atc/stup-list.png)

## Les CTOTs
La Calculated Takeoff Time est l’heure calculée ou injectée dans le CDM qui permet de respecter les mesures de régulations en vigueur. On a deux cas de figures : 

- Événement majeur avec slots : Les CTOTs sont calculés en amont et sont fixées quelques jours/heures avant la date de l'événement. On injecte les CTOTs dans le CDM qui, après un calcul simple, nous renvoie les TSAT correspondantes. 

- Événement normal avec mesures de régulation : le CDM est restreint par les MDI (Minimum Departure Interval) imposés ainsi que la capacité de piste. Le CDM calcule alors une CTOT respectant cette mesure et renvoie une TSAT de la même manière que mentionné précédemment. 

> Seule une CTOT imposée par une mesure de régulation est variable, c’est-à-dire que le délai peut être ajusté dans le temps par le CDM en fonction de l’évolution des autres aéronefs. 
{.is-info}


# Logique de la GLD
La GLD est un système complexe qui optimise en permanence la séquence de départ.
Afin de mieux la comprendre, voici son fonctionnement simplifié dans différentes situations.

Dès qu'un trafic se connecte au sol d’un aéroport où le CDM est en opération, la GLD récupère l’EOBT du plan de vol et l’affiche en tant que TOBT. Dans ce cas, la TOBT apparaît en vert clair (c’est une TOBT non confirmée). 
Cette première estimation de TOBT permet à la GLD de calculer une TTOT initiale avec le calcul suivant : 
**<p align=center>TOBT + EXOT = TTOT</p>**

L’EXOT ou Estimated Taxi-Out Time est défini dans la configuration de l’aéroport, la valeur diffère selon la zone de stationnement et la piste de départ.
La TTOT ainsi obtenue permet de vérifier si la capacité de piste n’est pas dépassée.
On a donc deux cas possibles : 

- celui où la capacité de piste n’est pas dépassée (optimal)
- celui où la capacité de piste est dépassée.

Cette capacité est définie dans la configuration de l’aéroport.
Si le nombre de départs est inférieur à la capacité, la GLD effectue alors le calcul suivant pour déterminer la TSAT : 

**<p align=center>TSAT = TTOT - EXOT</p>**

Si le nombre de départs est supérieur à la capacité sur le bloc correspondant, alors la GLD place le trafic dans le prochain bloc dont la capacité n’est pas dépassée.

<u>Exemple</u> : Une TTOT initiale à 1157Z est dans le bloc de 1150Z à 1200Z. Le bloc est à capacité maximale alors, la TTOT est décalée à 1200Z (première heure disponible si le bloc de 1200Z à 1210Z n’est pas à capacité maximale).

La GLD effectue alors le calcul précédent : TSAT = TTOT - EXOT
Dans ce cas ci, la TSAT peut différer de la TOBT, si cette différence est supérieure à 5 minutes, on parle alors de retard au bloc ou start-up delay. Cette situation est visible dans la start-up list comme expliqué dans la partie [TOBT](#La-TOBT).

En plus de cette vérification de capacité, la GLD va assurer le respect des mesures ECFMP de type MDI (Minimum Departure Interval), seule mesure prise en charge pour le moment.

Pour le faire, elle vérifie d’abord qu’une mesure active existe entre le départ (où le CDM est en opération) et la destination. Elle vérifie ensuite dans un bloc le nombre de départs vers une cette destination est si la valeur de la MDI est respectée.

<u>Exemple</u> : Lors d’un Paris By Night, une MDI de 6 minutes est demandée par EDDF au départ de Charles De Gaulle et à destination de Frankfurt. La GLD vérifie donc qu’il y ait bien 6 minutes entre chaque départ à destination de Frankfurt dans chaque bloc temps.

Dans ce cas : La GLD génère un CTOT, celui-ci sert à décaler la TTOT du second départ au premier créneau disponible permettant le respect de la mesure, on parle ici d’un Calculated Take Off Time. La TSAT est alors recalculée avec le calcul suivant : 

**<p align=center>TSAT = CTOT - EXOT</u>**

Contrairement à un CTOT réservé pour un événement (indiqué par un **<span style="color:green">B</span>** dans la startup list) comme le Cross The Pond/Land, un CTOT imposé pour respecter une mesure peut s’améliorer (c'est-à-dire, réduire le retard au bloc) en fonction de l’évolution des TOBTs des trafics impactés par la mesure.

# Utilisation
## Généralités
Pour démontrer l’utilisation en tant que contrôleur du CDM, nous allons suivre un trafic fictif au départ.
Tout d’abord, si vous êtes connecté en tant que sol ou prévol vous devez utiliser la commande “.vacdm master” seulement après avoir défini les pistes en service. Ceci vous permet d’interagir avec la GLD. Si vous êtes connecté en tant que tour vous n’avez rien à faire.

Pour commencer, lorsque le trafic se connecte, le plugin récupère le plan de vol pour en extraire l’EOBT. Cette valeur va servir à la GLD comme expliqué en partie 3 ([Logique de la GLD](#logique-de-la-gld)).

> Un trafic qui n’a pas d’EOBT ne sera pas pris en compte dans la séquence de départ.
{.is-info}

Notre trafic fictif va donc recevoir une TSAT calculée par la GLD, celle-ci donne lieu à 4 situations possibles visibles dans l’exemple ci-dessous.

![cdm-use.png](/doc-atc/cdm-use.png)

Il est important de comprendre l’affichage de la startup list car elle donne de manière précise l’état d’un trafic dans la séquence de départ. Pour vous aider à mieux comprendre les couleurs expliquées dans la partie sur Les horaires clés, voici la description des 4 trafics de l’exemple.

- EJU56VC : TOBT et TSAT <span style="color:orange">ORANGE</span>, créneau manqué (la TOBT expire lorsque la TSAT expire, soit à TSAT + 5 minutes). Le trafic doit envoyer une nouvelle TOBT.

- TVF204 : La TOBT en <span style="color:green">VERT</span> indique qu’elle est confirmée. Sa TSAT et également <span style="color:green">VERTE</span>, cela indique que le trafic peut être transféré au sol pour demander le repoussage.

- AFR4240 : La TOBT ainsi que la TSAT en <span style="color:yellowgreen">VERT CLAIR</span> indique 2 choses. D’abord que la TOBT n’est pas confirmée mais est dans le futur (et dans - d’une heure). Et ensuite que la TSAT n’est <u>pas encore</u> valide.
 
- AFR62BT : La TOBT <span style="color:yellow">JAUNE CLAIR</span> indique 2 choses, tout d’abord que le trafic subit un retard au bloc et ensuite que sa TOBT n’est pas confirmée (sinon la TOBT serait <span style="color:gold">JAUNE</span>). La TSAT <span style="color:royalblue">BLEUE</span> indique elle la raison du retard car il s’agit d’un CTOT ici dû à un booking (le **<span style="color:green">B</span>** visible à droite du CTOT). Vous n’avez alors jusqu’ici en tant que contrôleur rien à gérer.

## La Prévol
Votre première vraie action sera au moment où le trafic demande sa clairance de départ. 
En plus de sa clairance, vous devrez lui indiquer sa TSAT si sa TOBT est confirmée et valide (<span style="color:green">VERTE</span>) et son CTOT (s’il y en a un).

Si sa TOBT n’est pas confirmée (<span style="color:yellowgreen">VERT CLAIR</span>), vous devrez alors demander au trafic d’envoyer une TOBT sur le <a href="https://cdm.vatsim.fr" target="_blank">site du CDM</a> ou bien de vous donner son heure estimée de repoussage et l’ajouter manuellement à la GLD. Pour le faire, il faut cliquer sur la TOBT, un menu déroulant apparaît avec 3 options (image ci-dessous).
![tobt-menu.png](/doc-atc/tobt-menu.png)
Si la TOBT donnée par le trafic correspond à son EOBT alors il suffit de cliquer sur “TOBT confirm”, si elle est différente il faut cliquer sur “TOBT edit” et entrer l’heure donnée.

Plus tard, si le trafic appelle prêt pour le repoussage mais que sa TSAT n’est pas encore valide (<span style="color:yellowgreen">VERT CLAIR</span>), vous devrez noter l’heure actuelle en cliquant sur son ASRT (Actual Startup Request Time). Lorsque sa TSAT est valide alors vous pouvez le transférer au sol.

En tant que DEL, au moment du transfert vers le sol, il faut noter l’ASAT (Actual Startup Approval Time) en cliquant dessus dans la liste. L’heure actuelle apparaît alors comme ASAT pour tous les autres contrôleurs qui savent donc si le trafic est relâché par la prévol. 

<u>Petit +</u> : Le fait de cliquer-droit sur ASAT définit également le statut STUP au trafic en question. Ceci est utile lorsqu’il s’agit d’un stand autonome ou que le GND demande le statut pour les trafics relâchés.

## Le Sol
En tant que GND, une fois que le trafic envoyé par la DEL est en fréquence, vous devez noter l’AORT (Actual Off block Request Time) ou l’AOBT (Actual Off Block Time) selon les  situations suivantes : 

- Si vous ne pouvez pas directement l’autoriser au repoussage, il faut noter l’AORT. 
L’AORT vous sert d’aide-mémoire en plus de la Request list (par exemple, le trafic est en fréquence et prêt à repousser mais retenu cause trafic).
- Si le trafic est autorisé au repoussage, vous devez noter son AOBT.

Lorsque que vous notez l’AOBT d’un trafic, le statut PUSH s’ajoute automatiquement à ce trafic.
L’utilisation des horaires de request indique également au contrôleur précédent que le trafic est en contact sur la bonne fréquence. Dans le cas où il n’y a pas de contrôleur DEL, vous devez également gérer les horaires. L’ASAT et l’AOBT ne sont à noter qu’avec la clairance à laquelle elles correspondent. Une fois que le trafic est autorisé au repoussage et que son AOBT est notée, il n’y a plus d’action CDM à effectuer. Au sol, il faudra donc répartir les trafics sur différents points d'attente ou les séquencer en amont pour assurer la fluidité au départ en cas de mesures.

## La Tour
Le contrôleur tour doit quant à lui assurer le respect des CTOTs lorsqu’il y en a.

La tour en coordination avec le sol surveille également la fluidité des départs, de nombreux TTOT oranges sont le résultat de différents facteurs, un temps de roulage non-optimum dans la  configuration, un roulage trop lent, trop d’attente à la piste.

![cdm-hp.png](/doc-atc/cdm-hp.png)

> Le CDM n’empêche pas la file d’attente en proximité de piste. En revanche, <u>une bonne utilisation de l’outil permet de la limiter</u>. Le CDM cherche à optimiser la séquence de départ en se basant sur la capacité piste qui a été définie. Il propose donc d’envoyer le juste nombre de trafics au point d’attente dans un bloc temps défini.
{.is-info}