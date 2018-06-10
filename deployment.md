# Votre contrat
Félicitations, votre contrat est désormais terminé !
Voici ci-dessous une des implémentations possibles de ce contrat :

> Require ne permettant pour le moment pas de retourner de message d'erreur, dans le cas où c'est bien le propriétaire du contrat, j'ai décidé de renvoyer un message d'erreur au lieu de juste faire un require

```javascript
pragma solidity ^0.4.24;

contract CapsuleTemporelle {
    string message;
    address owner;
    uint creationtime;


    constructor(string _message) public {
        message = _message;
        owner = msg.sender;
        creationtime = block.timestamp;
    }

    function getMessage() public view returns (string) {
        require(owner == msg.sender);
        if (now > creationtime + 365 * 1 days) {
            return message;
        } else {
            return "Vous ne pouvez pas lire le message avant 1 an !";
        }
    }

}
```


# Déploiement du contrat #1

Actuellement sur https://remix.ethereum.org/ nous avons utilisé les paramètres par défaut, soit la VM javascript pour faire nos tests. Nous n'avons pas directement publié le contrat sur la blockchain. C'est donc le moment de le faire !

# Créer une adresse ethereum

Pour interagir avec la blockchain il vous faut une adresse ethereum.
Nous allons utiliser Metamask pour la créer, et pour interagir avec Ethereum depuis votre navigateur : https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn

Après l'installation, cliquez sur l'icône de Metamask en haut à droite de votre navigateur, acceptez les conditions d'utilisations et définissez un mot de passe.

# Récupérer des tokens

Pour éviter de devoir dépenser de l'argent pour acheter des tokens, nous allons nous mettre sur un testnet Ethereum.
Pour cela cliquez en haut à gauche de Metamask et choissisez Ropsten test network puis cliquez sur buy puis enfin ROPSTEN TEST FAUCET. Sur le site, cliquez sur "request 1 ether from faucet".
Après quelques minutes, vous voilà désormais en possession d'un ether sur le testnet !

# Déploiement du contrat #2

Retournez sur https://remix.ethereum.org/, rendez-vous sur l'onglet RUN en haut à droite, cliquez sur ENVIRONNEMENT et choissisez Injected Web3.
Vous pouvez désormais remplir le champ message (situé à côté du bouton rouge deploy).
> ATTENTION: Il faut mettre votre message entre guillemets pour que cela fonctionne.
Cliquez sur Deploy, et sur submit sur la fenêtre Metamask qui s'affiche.
Une adresse s'affiche dans le terminal, c'est l'adresse de votre contrat sur le testnet Ethereum ! Félicitations !
