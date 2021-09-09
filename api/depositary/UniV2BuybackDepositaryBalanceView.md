## UniV2BuybackDepositaryBalanceView





### Events
```solidity
IssuerChanged(address newIssuer)
```

An event that is emitted when an issuer contract address changed.



```solidity
UniswapRouterChanged(address newRouter)
```

An event that is emitted when an Uniswap router contract address changed.



```solidity
CallerChanged(address newCaller)
```

An event that is emitted when an caller wallet changed.



```solidity
Buyback(uint256 amount, uint256 buy)
```

An event that is emitted when an contract buyback stable token.




### Variables
```solidity
uint256 decimals
```

```solidity
contract ERC20 token
```

```solidity
contract Issuer issuer
```

```solidity
contract IUniswapV2Router02 uniswapRouter
```

```solidity
address caller
```


### Functions
```solidity
constructor(address _token, address _issuer, address _uniswapRouter, address _caller)
```





```solidity
changeIssuer(address _issuer)
```

Change issuer contract address.




**Arguments:**
- *_issuer* - New issuer contract address.

```solidity
changeUniswapRouter(address _uniswapRouter)
```

Change Uniswap router contract address.




**Arguments:**
- *_uniswapRouter* - New Uniswap router contract address.

```solidity
changeCaller(address _caller)
```

Change caller wallet.




**Arguments:**
- *_caller* - New caller wallet.

```solidity
transfer(address _token, address recipient, uint256 amount)
```

Transfer token to recipient.




**Arguments:**
- *_token* - Target token.

- *recipient* - Address of recipient.

- *amount* - Amount of transferred token.

```solidity
buy(uint256 amount)
```

Buyback stable token from Uniswap pool.




**Arguments:**
- *amount* - Amount of buyback token.

```solidity
balance() → uint256
```

Get balance of depositary.




**Returns:**
- *Balance* - of depositary.

