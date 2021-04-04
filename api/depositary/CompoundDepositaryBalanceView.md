## CompoundDepositaryBalanceView





### Events
```solidity
Invested(address cToken, uint256 amount)
```

An event thats emitted when an invested token.



```solidity
Withdrawal(address cToken, uint256 amount, uint256 profit, address investRecipient, address profitRecipient)
```

An event thats emitted when an withdrawal token.




### Variables
```solidity
uint256 decimals
```

```solidity
mapping(address => uint256) balances
```


### Functions
```solidity
balanceOf(address cToken) → uint256
```





**Arguments:**
- *cToken* - Invested cToken.


**Returns:**
- *Balance* - of invested token.

```solidity
invest(address cToken, uint256 amount)
```

Invest token to Compound.




**Arguments:**
- *cToken* - Invested cToken. Target ERC20 token should be approved to contract before call.

- *amount* - Amount of invested token.

```solidity
withdraw(address cToken, address investRecipient, address profitRecipient)
```

Withdraw invested token and reward.




**Arguments:**
- *cToken* - Invested cToken.

- *investRecipient* - Recipient of invested token.

- *profitRecipient* - Recipient of reward token.

```solidity
investedTokens() → address[]
```





**Returns:**
- *Invested* - cTokens.

```solidity
balance() → uint256
```





