## BuybackDepositaryBalanceView





### Events
```solidity
IssuerChanged(address newIssuer)
```

An event that is emitted when an issuer contract address changed.



```solidity
Buyback(address customer, uint256 amount, uint256 buy)
```

An event that is emitted when an account buyback stable token.




### Variables
```solidity
uint256 decimals
```

```solidity
contract ERC20 product
```

```solidity
contract Issuer issuer
```


### Functions
```solidity
constructor(address _issuer, address _product)
```





**Arguments:**
- *_issuer* - Issuer contract address.

- *_product* - Product token address.

```solidity
changeIssuer(address _issuer)
```

Change issuer contract address.




**Arguments:**
- *_issuer* - New issuer contract address.

```solidity
transferProductToken(address recipient, uint256 amount)
```

Transfer product token.




**Arguments:**
- *recipient* - Address of recipient.

- *amount* - Amount of transferred token.

```solidity
transferStableToken(address recipient, uint256 amount)
```

Transfer stable token.




**Arguments:**
- *recipient* - Address of recipient.

- *amount* - Amount of transferred token.

```solidity
buy(uint256 amount)
```

Buyback stable token.




**Arguments:**
- *amount* - Amount of payment token.

```solidity
balance() → uint256
```





