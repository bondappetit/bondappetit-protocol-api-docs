## Investment





### Events
```solidity
UniswapRouterChanged(address newUniswapRouter)
```

An event thats emitted when an uniswap router contract address changed.



```solidity
InvestTokenAllowed(address token)
```

An event thats emitted when an invest token allowed.



```solidity
InvestTokenDenied(address token)
```

An event thats emitted when an invest token denied.



```solidity
GovernanceTokenPriceChanged(uint256 newPrice)
```

An event thats emitted when an governance token price changed.



```solidity
Invested(address investor, address token, uint256 amount, uint256 reward)
```

An event thats emitted when an invested token.



```solidity
Withdrawal(address recipient, address token, uint256 amount)
```

An event thats emitted when an withdrawal token.




### Variables
```solidity
contract ERC20 cumulative
```

```solidity
contract GovernanceToken governanceToken
```

```solidity
uint256 governanceTokenLockDate
```

```solidity
uint8 GOVERNANCE_TOKEN_PRICE_DECIMALS
```

```solidity
uint256 governanceTokenPrice
```

```solidity
contract IUniswapV2Router02 uniswapRouter
```

```solidity
mapping(address => bool) investmentTokens
```


### Functions
```solidity
constructor(address _cumulative, address _governanceToken, uint256 _governanceTokenLockDate, address _uniswapRouter)
```





**Arguments:**
- *_cumulative* - Address of cumulative token

- *_governanceToken* - Address of governance token

- *_uniswapRouter* - Address of UniswapV2Router

```solidity
changeUniswapRouter(address _uniswapRouter)
```

Changed uniswap router contract address.




**Arguments:**
- *_uniswapRouter* - Address new uniswap router contract.

```solidity
allowToken(address token)
```

Add token to investable tokens white list




**Arguments:**
- *token* - Allowable token

```solidity
denyToken(address token)
```

Remove token from investable tokens white list




**Arguments:**
- *token* - Denied token

```solidity
changeGovernanceTokenPrice(uint256 newPrice)
```

Update governance token price




**Arguments:**
- *newPrice* - New price of governance token of USD (6 decimal)

```solidity
price(address token, uint256 amount) → uint256
```





**Arguments:**
- *token* - Invested token

- *amount* - Invested amount


**Returns:**
- *Amount* - governance token after swap

```solidity
invest(address token, uint256 amount) → bool
```

Invest tokens to protocol




**Arguments:**
- *token* - Invested token

- *amount* - Invested amount

```solidity
investETH() → bool
```

Invest ETH to protocol



```solidity
withdraw(address recipient)
```

Withdraw invested token to address




**Arguments:**
- *recipient* - Recipient of tokens

