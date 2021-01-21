## Market





### Events
```solidity
PriceOracleChanged(address newPriceOracle)
```

An event thats emitted when an price oracle contract address changed.



```solidity
UniswapRouterChanged(address newUniswapRouter)
```

An event thats emitted when an uniswap router contract address changed.



```solidity
CumulativeChanged(address newToken)
```

An event thats emitted when an cumulative token changed.



```solidity
TokenAllowed(address token, string symbol)
```

An event thats emitted when an token allowed.



```solidity
TokenDenied(address token)
```

An event thats emitted when an token denied.



```solidity
GovernanceTokenPriceChanged(uint256 newPrice)
```

An event thats emitted when an governance token price changed.



```solidity
Buy(address customer, address product, address token, uint256 amount, uint256 buy)
```

An event thats emitted when an account buyed token.



```solidity
Withdrawal(address recipient, address token, uint256 amount)
```

An event thats emitted when an cumulative token withdrawal.




### Variables
```solidity
uint256 PRICE_DECIMALS
```

```solidity
contract ERC20 cumulative
```

```solidity
contract ERC20 stableToken
```

```solidity
contract ERC20 governanceToken
```

```solidity
uint256 governanceTokenPrice
```

```solidity
contract IUniswapV2Router02 uniswapRouter
```

```solidity
contract IUniswapAnchoredView priceOracle
```

```solidity
mapping(address => string) allowedTokens
```


### Functions
```solidity
constructor(address _cumulative, address _stableToken, address _governanceToken, address _uniswapRouter, address _priceOracle)
```





**Arguments:**
- *_cumulative* - Address of cumulative token.

- *_stableToken* - Address of stable token.

- *_governanceToken* - Address of governance token.

- *_uniswapRouter* - Address of Uniswap router contract.

- *_priceOracle* - Address of Price oracle contract.

```solidity
changeUniswapRouter(address _uniswapRouter)
```

Changed uniswap router contract address.




**Arguments:**
- *_uniswapRouter* - Address new uniswap router contract.

```solidity
changePriceOracle(address _priceOracle)
```

Changed price oracle contract address.




**Arguments:**
- *_priceOracle* - Address new price oracle contract.

```solidity
changeCumulativeToken(address newToken, address recipient)
```

Changed cumulative token address.




**Arguments:**
- *newToken* - Address new cumulative token.

- *recipient* - Address of recipient for withdraw current cumulative balance.

```solidity
allowToken(address token, string symbol)
```

Add token to tokens white list.




**Arguments:**
- *token* - Allowable token.

- *symbol* - Symbol target token of price oracle contract.

```solidity
denyToken(address token)
```

Remove token from tokens white list.




**Arguments:**
- *token* - Denied token.

```solidity
isAllowedToken(address token) → bool
```





**Arguments:**
- *token* - Target token.


**Returns:**
- *Is* - target token allowed.

```solidity
changeGovernanceTokenPrice(uint256 newPrice)
```

Update price of governance token.




**Arguments:**
- *newPrice* - New price of governance token of USD (6 decimal).

```solidity
transferStableToken(address recipient, uint256 amount)
```

Transfer stable token to recipient.




**Arguments:**
- *recipient* - Address of recipient.

- *amount* - Amount of transfered token.

```solidity
transferGovernanceToken(address recipient, uint256 amount)
```

Transfer governance token to recipient.




**Arguments:**
- *recipient* - Address of recipient.

- *amount* - Amount of transfered token.

```solidity
priceStableToken(address token, uint256 amount) → uint256
```



Get stable token price from payment token amount.


**Arguments:**
- *token* - Payment token.

- *amount* - Payment token amount.


**Returns:**
- *Price* - of product token.

```solidity
priceGovernanceToken(address token, uint256 amount) → uint256
```



Get governance token price from payment token amount.


**Arguments:**
- *token* - Payment token.

- *amount* - Payment token amount.


**Returns:**
- *Price* - of product token.

```solidity
buyStableToken(address token, uint256 amount) → bool
```

Buy stable token with ERC20 payment token amount.




**Arguments:**
- *token* - Payment token.

- *amount* - Amount of payment token.


**Returns:**
- *True* - if success.

```solidity
buyGovernanceToken(address token, uint256 amount) → bool
```

Buy governance token with ERC20 payment token amount.




**Arguments:**
- *token* - Payment token.

- *amount* - Amount of payment token.


**Returns:**
- *True* - if success.

```solidity
buyStableTokenFromETH() → bool
```

Buy stable token with ETH amount.




**Returns:**
- *True* - if success.

```solidity
buyGovernanceTokenFromETH() → bool
```

Buy governance token with ETH amount.




**Returns:**
- *True* - if success.

```solidity
withdraw(address recipient)
```

Withdraw cumulative token to address.




**Arguments:**
- *recipient* - Recipient of token.

