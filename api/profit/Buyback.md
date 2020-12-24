## Buyback





### Events
```solidity
Transfer(address recipient, uint256 amount)
```

An event thats emitted when an incoming token transferred to recipient.



```solidity
RecipientChanged(address newRecipient)
```

An event thats emitted when an recipient address changed.



```solidity
IncomingChanged(address newIncoming)
```

An event thats emitted when an incoming token changed.



```solidity
UniswapRouterChanged(address newUniswapRouter)
```

An event thats emitted when an uniswap router contract address changed.



```solidity
BuybackSuccessed(uint256 incoming, uint256 outcoming)
```

An event thats emitted when an buyback successed.




### Variables
```solidity
contract ERC20 incoming
```

```solidity
contract ERC20 outcoming
```

```solidity
address recipient
```

```solidity
contract IUniswapV2Router02 uniswapRouter
```


### Functions
```solidity
constructor(address _incoming, address _outcoming, address _recipient, address _uniswapRouter)
```





**Arguments:**
- *_incoming* - Address of incoming token.

- *_outcoming* - Address of outcoming token.

- *_recipient* - Address of recipient outcoming token.

- *_uniswapRouter* - Address of Uniswap router contract.

```solidity
changeRecipient(address _recipient)
```

Change recipient address.




**Arguments:**
- *_recipient* - New recipient address.

```solidity
changeUniswapRouter(address _uniswapRouter)
```

Changed uniswap router contract address.




**Arguments:**
- *_uniswapRouter* - Address new uniswap router contract.

```solidity
transfer(address _recipient, uint256 amount)
```

Transfer incoming token to recipient.




**Arguments:**
- *_recipient* - Address of recipient.

- *amount* - Amount of transferred token.

```solidity
changeIncoming(address _incoming, address _recipient)
```

Change incoming token address.




**Arguments:**
- *_incoming* - New incoming token address.

- *_recipient* - Address of recipient.

```solidity
buy(uint256 amount)
```

Make buyback attempt.




**Arguments:**
- *amount* - Amount of tokens to buyback.

