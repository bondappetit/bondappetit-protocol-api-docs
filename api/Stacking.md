## Stacking





### Events
```solidity
RewardChanged(address token, uint256 from, uint256 to)
```

An event thats emitted when an token reward changed.



```solidity
Locked(address account, address token, uint256 amount)
```

An event thats emitted when a token is locked by an account.



```solidity
Unlocked(address account, address token)
```

An event thats emitted when a token is unlocked by an account.




### Variables
```solidity
contract ERC20 rewardToken
```

```solidity
mapping(address => struct Stacking.Reward) rewards
```

```solidity
mapping(address => mapping(address => struct Stacking.Balance)) balances
```


### Functions
```solidity
constructor(address _rewardToken)
```





**Arguments:**
- *_rewardToken* - Address of reward token contract.

```solidity
changeReward(address token, uint256 newDelta)
```

Change reward token delta.




**Arguments:**
- *token* - Changed token address.

- *newDelta* - New reward delta.

```solidity
price(address token) → uint256
```

Get current price of token.




**Arguments:**
- *token* - Address of token.


**Returns:**
- *Price* - of token.

```solidity
reward(address token) → uint256
```

Get current reward of token for sender.




**Arguments:**
- *token* - Address of token.


**Returns:**
- *Reward* - of token for sender.

```solidity
lock(address token, uint256 amount)
```

Stacking token.




**Arguments:**
- *token* - Address of stacking token.

- *amount* - Amount of stacking token.

```solidity
unlock(address token)
```

Unstacking token.




**Arguments:**
- *token* - Address of unstacking token.

