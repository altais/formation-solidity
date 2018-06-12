# 1
```javascript
pragma solidity ^0.4.24;

contract TimeCapsule {

}
```

# 2
```javascript
pragma solidity ^0.4.24;

contract TimeCapsule {
	string message;
	address owner;
	uint creationTime;

}
```

# 3
```javascript
pragma solidity ^0.4.24;

contract TimeCapsule {
	string message;
	address owner;
	uint creationTime;

	constructor(string _message) public {
        message = _message;
	}

	function getMessage() public view returns (string _message) {
        return message;
    }
}
```

# 4
```javascript
pragma solidity ^0.4.24;

contract TimeCapsule {
	string message;
	address owner;
	uint creationTime;

	constructor(string _message) public {
		message = _message;
		creationTime = now;
	}

	function getMessage() public view returns (string _message) {
        return message;
    }
}
```

# 5
```javascript
pragma solidity ^0.4.24;

contract TimeCapsule {
	string message;
	address owner;
	uint creationTime;

	constructor(string _message) public {
		message = _message;
		creationTime = now;
		owner = msg.sender;
	}

	function getMessage() public view returns (string _message) {
        return message;
    }
}
```

# 6
```javascript
pragma solidity ^0.4.24;

contract TimeCapsule {
	string message;
	address owner;
	uint creationTime;

	constructor(string _message) public {
		message = _message;
		creationTime = now;
		owner = msg.sender;
	}

	function getMessage() public view returns (string _message) {
		require(owner == msg.sender);
		if (now > creationTime + 365 days) {
            return message;
        } else {
            return "Vous ne pouvez pas lire le message avant 1 an !";
        }
    }
}
```
