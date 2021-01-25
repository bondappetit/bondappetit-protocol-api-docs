## StableTokenDepositaryBalanceView





### Events
```solidity
TokenAllowed(address token)
```

An event emitted when token allowed.



```solidity
TokenDenied(address token)
```

An event emitted when token denied.




### Variables
```solidity
uint256 decimals
```


### Functions
```solidity
allowToken(address token)
```

Allow token.




**Arguments:**
- *token* - Allowed token.

```solidity
denyToken(address token)
```

Deny token.




**Arguments:**
- *token* - Denied token.

```solidity
transfer(address token, address recipient, uint256 amount)
```

Transfer target token to recipient.




**Arguments:**
- *token* - Target token.

- *recipient* - Recipient.

- *amount* - Transfer amount.

```solidity
allowedTokens() → address[]
```





**Returns:**
- *Allowed* - tokens list.

```solidity
balance() → uint256
```





