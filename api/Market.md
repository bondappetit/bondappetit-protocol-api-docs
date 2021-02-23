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
Buy(address customer, address token, uint256 amount, uint256 buy, uint256 reward)
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
uint256 REWARD_DECIMALS
```

```solidity
contract ERC20 cumulative
```

```solidity
contract ERC20 productToken
```

```solidity
contract ERC20 rewardToken
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
constructor(address _cumulative, address _productToken, address _rewardToken, address _uniswapRouter, address _priceOracle)
```





**Arguments:**
- *_cumulative* - Address of cumulative token.

- *_productToken* - Address of product token.

- *_rewardToken* - Address of reward token.

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
transferProductToken(address recipient, uint256 amount)
```

Transfer product token to recipient.




**Arguments:**
- *recipient* - Address of recipient.

- *amount* - Amount of transfered token.

```solidity
transferRewardToken(address recipient, uint256 amount)
```

Transfer reward token to recipient.




**Arguments:**
- *recipient* - Address of recipient.

- *amount* - Amount of transfered token.

```solidity
price(address currency, uint256 payment) → uint256 product, uint256 reward
```

Get token price.




**Arguments:**
- *currency* - Currency token.

- *payment* - Amount of payment.


**Returns:**
- *product* - Amount of product token.

- *reward* - Amount of reward token.

```solidity
buy(address currency, uint256 payment) → bool
```

Buy token with ERC20.




**Arguments:**
- *currency* - Currency token.

- *payment* - Amount of payment.


**Returns:**
- *True* - if success.

```solidity
buyFromETH() → bool
```

Buy token with ETH.




**Returns:**
- *True* - if success.

```solidity
withdraw(address recipient)
```

Withdraw cumulative token to address.




**Arguments:**
- *recipient* - Recipient of token.

