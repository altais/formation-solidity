# Require

Maintenant que nous avons enregistré notre propriétaire, il faut limiter l'accès.
En Solidity, il faut utiliser le mot-clé require qui va faire en sorte que la fonction s’arrête et renvoie une erreur si certaines conditions ne sont pas respectées :

```javascript
pragma solidity ^0.4.24;
contract Example {

	function olderThan21 (uint _age) public {
		require(_age > 21);
		// do your stuff
	}
}
```
Si la personne a moins de 21 ans, la fonction s'arrête immédiatement et rembourse le gas restant à l'utilisateur.

# A vous de jouer :
> * Limiter l'accès à votre fonction get() pour n'autoriser que le propriétaire
> * Limiter l'accès à votre fonction get() pour ne pas renvoyer le message avant 1 an

Félicitations, votre contrat est désormais terminé !
