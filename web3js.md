# Intro à Web3.js

Maintenant que notre contrat est déployé, [voici une page web](https://altais.github.io/formation-solidity/interface.html) très basique vous permettant de voir votre message dans 1 an.
Elle restera en ligne et vous permettra de voir votre message dans 1 an si vous le souhaitez :-)

> ATTENTION: Il faudra réinstaller Metamask sur votre PC et importer votre clé privée !

Sur cette page il vous suffit de rentrer l'adresse Ethereum de votre contrat pour pouvoir récupérer le message.

Pour tester au mieux votre contrat, je vous suggère de modifier la durée de 1 an par 1 `minutes` et de redéployer votre contrat.

Vous pouvez donc voir votre message au bout de 1 min, et si vous essayez depuis le PC de votre voisin, aucun message ne s'affichera.

# Mais en fait...

Et pourtant si votre voisin veut lire votre message, malgré vos restrictions, il peut le faire !

Ce tutoriel avait pour but de vous montrer comment écrire un contrat et le déployer, mais aussi de vous mettre en garde :

Une blockchain est intrinsèquement publique : tout ce qui est dessus peut être lu par absolument tout le monde.

Votre fonction `getMessage()` ne peut en effet pas être appelé par quelqu'un d'autre que vous, et pas avant 1 an, mais vos variables, elles, sont lisibles !

La technologie blockchain est très puissante attention, un grand pouvoir implique de grandes responsabilités! Vous devez être conscient de ce genre de problématiques lorsque vous développez votre contrat, car un contrat déployé ne peut plus JAMAIS être modifié !

Je vous laisse chercher par vous même de quelle manière vous pouvez lire les messages malgré les restrictions ;)