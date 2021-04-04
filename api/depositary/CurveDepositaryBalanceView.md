## CurveDepositaryBalanceView





### Events
```solidity
RegistryChanged(address registry)
```

An event thats emitted when an curve registry address changed.



```solidity
MinterChanged(address minter)
```

An event thats emitted when an curve minter address changed.



```solidity
UniswapRouterChanged(address uniswapRouter)
```

An event thats emitted when an uniswap router address changed.



```solidity
Invested(address pool, address token, uint256 amount)
```

An event thats emitted when an invested token.



```solidity
Withdrawal(address token, uint256 amount, uint256 profit, address investRecipient, address profitRecipient)
```

An event thats emitted when an withdrawal token.




### Variables
```solidity
address registry
```

```solidity
address minter
```

```solidity
address uniswapRouter
```

```solidity
uint256 decimals
```

```solidity
mapping(address => uint256) balances
```


### Functions
```solidity
constructor(address _registry, address _minter, address _uniswapRouter)
```





**Arguments:**
- *_registry* - Curve registry contract address.

- *_minter* - Curve minter contract address.

- *_uniswapRouter* - Uniswap router contract address.

```solidity
changeRegistry(address _registry)
```





**Arguments:**
- *_registry* - New Curve registry contract address.

```solidity
changeMinter(address _minter)
```





**Arguments:**
- *_minter* - New Curve minter contract address.

```solidity
changeUniswap(address _uniswapRouter)
```





**Arguments:**
- *_uniswapRouter* - New Uniswap router contract address.

```solidity
balanceOf(address pool) → uint256
```





**Arguments:**
- *pool* - Invested pool.


**Returns:**
- *Balance* - of invested pool.

```solidity
mintCrv(address pool, address toToken, address recipient)
```

Mint CRV tokens and swap to target token.




**Arguments:**
- *pool* - Target liquidity pool.

- *toToken* - Target token.

- *recipient* - Recipient.

```solidity
invest(address pool, uint256 tokenIndex, uint256 amount)
```

Invest token to Curve.




**Arguments:**
- *pool* - Target liquidity pool.

- *tokenIndex* - Invested token index in the pool. Target ERC20 token should be approved to contract before call.

- *amount* - Amount of invested token.

```solidity
withdraw(address pool, uint256 tokenIndex, address investRecipient, address profitRecipient)
```

Withdraw invested token and reward.




**Arguments:**
- *pool* - Target liquidity pool.

- *tokenIndex* - Invested token index in the pool.

- *investRecipient* - Recipient of invested token.

- *profitRecipient* - Recipient of reward token.

```solidity
investedPools() → address[]
```





**Returns:**
- *Invested* - liquidity pools.

```solidity
balance() → uint256
```





