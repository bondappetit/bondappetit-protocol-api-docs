## CurveDepositaryBalanceView





### Events
```solidity
RegistryChanged(address registry)
```

An event thats emitted when an curve registry address changed.



```solidity
UniswapRouterChanged(address uniswapRouter)
```

An event thats emitted when an uniswap router address changed.



```solidity
Invested(address pool, address token, uint256 amount)
```

An event thats emitted when an invested token.



```solidity
Withdrawal(address token, uint256 amount, address recipient)
```

An event thats emitted when an withdrawal token.



```solidity
Mint(address token, uint256 amount, address recipient)
```

An event thats emitted when an withdrawal proft token.




### Variables
```solidity
contract IRegistry registry
```

```solidity
contract IUniswapV2Router02 uniswapRouter
```

```solidity
uint256 decimals
```

```solidity
mapping(address => uint256) balances
```


### Functions
```solidity
constructor(address _registry, address _uniswapRouter)
```





**Arguments:**
- *_registry* - Curve registry contract address.

- *_uniswapRouter* - Uniswap router contract address.

```solidity
changeRegistry(address _registry)
```





**Arguments:**
- *_registry* - New Curve registry contract address.

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
mint(address pool, address toToken, address recipient)
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
withdraw(address pool, uint256 tokenIndex, address recipient)
```

Withdraw invested token and reward.




**Arguments:**
- *pool* - Target liquidity pool.

- *tokenIndex* - Invested token index in the pool.

- *recipient* - Recipient of invested token.

```solidity
investedPools() → address[]
```





**Returns:**
- *Invested* - liquidity pools.

```solidity
balance() → uint256
```





