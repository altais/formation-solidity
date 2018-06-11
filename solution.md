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
	uint createdTime;

}
```

# 3
```javascript
pragma solidity ^0.4.24;

contract TimeCapsule {
	string message;
	address owner;
	uint createdTime;

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
	uint createdTime;

	constructor(string _message) public {
		message = _message;
		createdTime = now;
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
	uint createdTime;

	constructor(string _message) public {
		message = _message;
		createdTime = now;
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
	uint createdTime;

	constructor(string _message) public {
		message = _message;
		createdTime = now;
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
