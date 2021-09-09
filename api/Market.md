## Market





### Events
```solidity
UniswapRouterChanged(address newUniswapRouter)
```

An event thats emitted when an uniswap router contract address changed.



```solidity
CumulativeChanged(address newToken, address[] priceFeed)
```

An event thats emitted when an cumulative token changed.



```solidity
TokenAllowed(address token, address[] priceFeed)
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
uint8 PRICE_DECIMALS
```

```solidity
uint256 REWARD_DECIMALS
```

```solidity
contract ERC20 cumulative
```

```solidity
address[] cumulativePriceFeed
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
mapping(address => address[]) allowedTokens
```


### Functions
```solidity
constructor(address _cumulative, address _productToken, address _rewardToken, address _uniswapRouter, address[] _cumulativePriceFeed)
```





**Arguments:**
- *_cumulative* - Address of cumulative token.

- *_productToken* - Address of product token.

- *_rewardToken* - Address of reward token.

- *_uniswapRouter* - Address of Uniswap router contract.

- *_cumulativePriceFeed* - Price feeds chain of cumulative token.

```solidity
changeUniswapRouter(address _uniswapRouter)
```

Changed uniswap router contract address.




**Arguments:**
- *_uniswapRouter* - Address new uniswap router contract.

```solidity
changeCumulativeToken(address newToken, address[] newCumulativePriceFeed, address recipient)
```

Changed cumulative token address.




**Arguments:**
- *newToken* - Address new cumulative token.

- *newCumulativePriceFeed* - Address new price oracle contract.

- *recipient* - Address of recipient for withdraw current cumulative balance.

```solidity
allowToken(address token, address[] priceFeed)
```

Add token to tokens white list.




**Arguments:**
- *token* - Allowable token.

- *priceFeed* - Price feed chain.

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
_priceUSD(address token) → uint256
```





**Arguments:**
- *token* - Target token.


**Returns:**
- *Price* - token at USD.

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

