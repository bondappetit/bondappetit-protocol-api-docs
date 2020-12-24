## UniswapMarketMaker





### Events
```solidity
TokenTransfer(address token, address recipient, uint256 amount)
```

An event thats emitted when an token transferred to recipient.



```solidity
UniswapRouterChanged(address newUniswapRouter)
```

An event thats emitted when an uniswap router contract address changed.



```solidity
IncomingChanged(address newIncoming)
```

An event thats emitted when an incoming token changed.



```solidity
LiquidityIncreased(uint256 incoming, uint256 support)
```

An event thats emitted when an liquidity added.



```solidity
LiquidityReduced(uint256 lp, uint256 incoming, uint256 support)
```

An event thats emitted when an liquidity removed.




### Variables
```solidity
contract ERC20 incoming
```

```solidity
contract ERC20 support
```

```solidity
contract IUniswapV2Router02 uniswapRouter
```


### Functions
```solidity
constructor(address _incoming, address _support, address _uniswapRouter)
```





**Arguments:**
- *_incoming* - Address of incoming token.

- *_support* - Address of support token.

- *_uniswapRouter* - Address of Uniswap router contract.

```solidity
transfer(address token, address recipient, uint256 amount)
```

Transfer incoming token to recipient.




**Arguments:**
- *token* - Address of transferred token.

- *recipient* - Address of recipient.

- *amount* - Amount of transferred token.

```solidity
changeUniswapRouter(address _uniswapRouter)
```

Changed uniswap router contract address.




**Arguments:**
- *_uniswapRouter* - Address new uniswap router contract.

```solidity
changeIncoming(address _incoming, address _recipient)
```

Change incoming token address.




**Arguments:**
- *_incoming* - New incoming token address.

- *_recipient* - Address of recipient.

```solidity
buyLiquidity(uint256 amount)
```

Buy support token and add liquidity.




**Arguments:**
- *amount* - Amount of incoming token.

```solidity
addLiquidity(uint256 incomingAmount, uint256 supportAmount)
```

Add liquidity.




**Arguments:**
- *incomingAmount* - Amount of incoming token.

- *supportAmount* - Amount of support token.

```solidity
liquidityPair() → address
```

Return liquidity pair address.




**Returns:**
- *Liquidity* - pair address.

```solidity
removeLiquidity(uint256 amount)
```

Remove liquidity.




**Arguments:**
- *amount* - Amount of liquidity pool token.

