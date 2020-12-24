## ProfitSplitter





### Events
```solidity
Transfer(address recipient, uint256 amount)
```

An event thats emitted when an incoming token transferred to recipient.



```solidity
BudgetChanged(address newBudget, uint256 newBalance)
```

An event thats emitted when an budget contract address and target balance changed.



```solidity
IncomingChanged(address newIncoming)
```

An event thats emitted when an incoming token changed.



```solidity
UniswapRouterChanged(address newUniswapRouter)
```

An event thats emitted when an uniswap router contract address changed.



```solidity
RecipientAdded(address recipient, uint256 share)
```

An event thats emitted when an recipient added.



```solidity
RecipientRemoved(address recipient)
```

An event thats emitted when an recipient removed.



```solidity
PayToBudget(address recipient, uint256 amount)
```

An event thats emitted when an profit payed to budget.



```solidity
PayToRecipient(address recipient, uint256 amount)
```

An event thats emitted when an profit payed to recipient.




### Variables
```solidity
uint256 SHARE_ACCURACY
```

```solidity
uint256 SHARE_DIGITS
```

```solidity
contract ERC20 incoming
```

```solidity
address payable budget
```

```solidity
uint256 budgetBalance
```

```solidity
mapping(address => uint256) shares
```

```solidity
contract IUniswapV2Router02 uniswapRouter
```


### Functions
```solidity
receive()
```





```solidity
constructor(address _incoming, address _uniswapRouter)
```





**Arguments:**
- *_incoming* - Address of incoming token.

- *_uniswapRouter* - Address of Uniswap router contract.

```solidity
changeUniswapRouter(address _uniswapRouter)
```

Changed uniswap router contract address.




**Arguments:**
- *_uniswapRouter* - Address new uniswap router contract.

```solidity
changeBudget(address payable _budget, uint256 _budgetBalance)
```

Changed budget contract address and target balance.




**Arguments:**
- *_budget* - Address of budget contract.

- *_budgetBalance* - Target budget balance.

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
addRecipient(address recipient, uint256 share)
```

Add recipient.




**Arguments:**
- *recipient* - Address of recipient contract.

- *share* - Target share.

```solidity
removeRecipient(address recipient)
```

Remove recipient.




**Arguments:**
- *recipient* - Address of recipient contract.

```solidity
getRecipients() → address[]
```

Get addresses of recipients.




**Returns:**
- *Current* - recipients list.

```solidity
split(uint256 amount)
```

Split all incoming token balance to recipients and budget contract.




**Arguments:**
- *amount* - Approved amount incoming token.

