## CollateralMarket





### Events
```solidity
TokenAllowed(address token)
```

An event emitted when token allowed.



```solidity
TokenDenied(address token)
```

An event emitted when token denied.



```solidity
IssuerChanged(address newIssuer)
```

An event thats emitted when an Issuer contract address changed.



```solidity
TreasuryChanged(address newTreasury)
```

An event thats emitted when an Treasury contract address changed.



```solidity
DepositaryChanged(address newDepositary)
```

An event thats emitted when an Depositary contract address changed.



```solidity
Buy(address customer, address token, uint256 amount, uint256 buy)
```

An event thats emitted when an account buyed token.




### Variables
```solidity
contract Issuer issuer
```

```solidity
contract Treasury treasury
```

```solidity
address depositary
```


### Functions
```solidity
constructor(address _issuer, address payable _treasury, address _depositary)
```





```solidity
allowToken(address token)
```

Allow token.




**Arguments:**
- *token* - Allowable token.

```solidity
denyToken(address token)
```

Deny token.




**Arguments:**
- *token* - Denied token.

```solidity
allowedTokens() → address[]
```





**Returns:**
- *Allowed* - tokens list.

```solidity
changeIssuer(address _issuer)
```

Change Issuer contract address.




**Arguments:**
- *_issuer* - New address Issuer contract.

```solidity
changeTreasury(address payable _treasury)
```

Change Treasury contract address.




**Arguments:**
- *_treasury* - New address Treasury contract.

```solidity
changeDepositary(address _depositary)
```

Change Depositary contract address.




**Arguments:**
- *_depositary* - New address Depositary contract.

```solidity
buy(contract ERC20 token, uint256 amount)
```

Buy stable token with ERC20 payment token amount.




**Arguments:**
- *token* - Payment token.

- *amount* - Amount of payment token.

