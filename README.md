# Chargeur de batterie sur Dynamo de moyeu de vélo

## Principe 
La dynamo est un générateur alternatif à 2 phases. Plus elle tourne vite, et plus la tension va être élevée.

On utilise un pont redresseur de tension pour donc redresser la tension alternative. J'ai choisi des diodes schottky qui ont une la chute de tension la plus faible ( en l'occurence 0.7V pour la SR560).

On va ensuite lisser la tension à l'aide de 2 condensateurs en parallèle (2 * 470 uF = 1000 uF) pour obtenir une tension continue.

Ensuite, on fait passer ça dans un convertisseur abaisseur de tension (buck) qui va ramener la tension à 5,1V. Le LM2596 se règle à l'aide d'une visse micrométrique qui permet de choisir la tension de sortie.

Il est préférable de charger une batterie type powerbank plutôt que par exemple un téléphone portable car ceux-ci n'apprécient pas trop des intensités variables de chargement ( proportionnelle à la vitesse du vélo)

## BOM (Bills of Material)
* Buck converter LM2596 35V 3A
* 4 Diodes de redressements schottky SR560 5A 60V
* Prise USB femelle
* 2 Condensateurs 470 uF 35V
* Perfoard

## Réalisation
![inside](/images/dynamo_usb.jpg)

## Rendement

La dynamo utilisée est une dynamo moyeu notée à 3W .
L'ampérage en sortie est mesurée à 0,42A environ pour une tension de 5,1V. Ce qui donne 2.1W donc un rendement d'environ 70%.
La tension à vide en sortie de redressage peut monter à plus de 30V.
Ce qui est étonnant, c'est que l'ampérage maximum est obtenu à une vitesse d'environ 20km/h et ne varie plus ensuite.
Je ne connais pas le fonctionnement interne de la dynamo.
