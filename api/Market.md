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
BondPriceChanged(uint256 newPrice)
```

An event thats emitted when an bond token price changed.



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
contract ABT abt
```

```solidity
contract Bond bond
```

```solidity
uint256 bondPrice
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
constructor(address _cumulative, address _abt, address _bond, address _uniswapRouter, address _priceOracle)
```





**Arguments:**
- *_cumulative* - Address of cumulative token.

- *_abt* - Address of ABT token.

- *_bond* - Address of Bond token.

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
changeBondPrice(uint256 newPrice)
```

Update Bond token price




**Arguments:**
- *newPrice* - New price of Bond token of USD (6 decimal)

```solidity
transferABT(address recipient, uint256 amount)
```

Transfer ABT token to recipient.




**Arguments:**
- *recipient* - Address of recipient.

- *amount* - Amount of transfered token.

```solidity
transferBond(address recipient, uint256 amount)
```

Transfer Bond token to recipient.




**Arguments:**
- *recipient* - Address of recipient.

- *amount* - Amount of transfered token.

```solidity
priceABT(address token, uint256 amount) → uint256
```



Get ABT token price from payment token amount.


**Arguments:**
- *token* - Payment token.

- *amount* - Payment token amount.


**Returns:**
- *Price* - of product token.

```solidity
priceBond(address token, uint256 amount) → uint256
```



Get Bond token price from payment token amount.


**Arguments:**
- *token* - Payment token.

- *amount* - Payment token amount.


**Returns:**
- *Price* - of product token.

```solidity
buyABT(address token, uint256 amount) → bool
```

Buy ABT token with ERC20 payment token amount.




**Arguments:**
- *token* - Payment token.

- *amount* - Amount of payment token.


**Returns:**
- *True* - if success.

```solidity
buyBond(address token, uint256 amount) → bool
```

Buy Bond token with ERC20 payment token amount.




**Arguments:**
- *token* - Payment token.

- *amount* - Amount of payment token.


**Returns:**
- *True* - if success.

```solidity
buyABTFromETH() → bool
```

Buy ABT token with ETH amount.




**Returns:**
- *True* - if success.

```solidity
buyBondFromETH() → bool
```

Buy Bond token with ETH amount.




**Returns:**
- *True* - if success.

```solidity
withdraw(address recipient)
```

Withdraw cumulative token to address.




**Arguments:**
- *recipient* - Recipient of token.

