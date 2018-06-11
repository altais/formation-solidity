# Variables

Maintenant que nous avons une structure pour notre contrat, pour qu'il fonctionne, nous allons devoir sauvegarder le message, la date de création du contrat, ainsi que le propriétaire.

Voyons voir comment Solidity gère les variables.

Les variables sont stockées de manière permanente dans le stockage du contrat. Cela signifie qu'elles sont écrites dans la blockchain Ethereum. C'est comme écrire dans une base de données.

```javascript
pragma solidity ^0.4.24;
contract Example {
  // Cela sera stocké de manière permanente dans la blockchain.
  uint myAge = 23;
}
```
Dans cet exemple de contrat, nous avons créé un `uint` appelé `myAge` qui a pour valeur 23.
Vous pouvez trouver tous les types disponibles [ici.](http://solidity.readthedocs.io/en/v0.4.24/types.html)

# À vous de jouer :
> Créer dans votre contrat les variables :
  * `message` de type `string`
  * `owner` de type `address`
  * `creationTime` de type `uint`
