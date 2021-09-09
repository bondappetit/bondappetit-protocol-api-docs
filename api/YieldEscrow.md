## YieldEscrow





### Events
```solidity
VoteDelegatorCreated(address account, address voteDelegator)
```





```solidity
VoteDelegatorDestroyed(address account)
```





```solidity
TransferAllowed(address account)
```





```solidity
TransferDenied(address account)
```





```solidity
Deposit(address account, uint256 amount)
```





```solidity
Withdraw(address account, uint256 amount)
```






### Variables
```solidity
address governanceToken
```

```solidity
address voteDelegatorPrototype
```

```solidity
mapping(address => address) _voteDelegators
```

```solidity
mapping(address => bool) _allowedTransferAddresses
```


### Functions
```solidity
constructor(address _governanceToken, address _voteDelegatorPrototype)
```





**Arguments:**
- *_governanceToken* - Governance token contract address.

```solidity
voteDelegatorOf(address account) → address
```





**Arguments:**
- *account* - Target account.


**Returns:**
- *Address* - of vote delegator (zero if not delegate).

```solidity
createVoteDelegator() → address
```

Create vote delegator contract for sender account.




**Returns:**
- *Address* - of vote delegator.

```solidity
allowTransfer(address account)
```

Allow transfer tokens for account.




**Arguments:**
- *account* - Target account.

```solidity
denyTransfer(address account)
```

Deny transfer tokens for account.




**Arguments:**
- *account* - Target account.

```solidity
deposit(uint256 amount)
```

Deposit governance token.




**Arguments:**
- *amount* - Deposit amount.

```solidity
depositFromDelegator(address account, uint256 amount)
```

Deposit governance token from vote delegator only.




**Arguments:**
- *account* - Target account.

- *amount* - Deposit amount.

```solidity
withdraw(uint256 amount)
```

Withdraw governance token.




**Arguments:**
- *amount* - Withdraw amount.

```solidity
withdrawFromDelegator(address account, uint256 amount)
```

Withdraw governance token from vote delegator only.




**Arguments:**
- *account* - Target account.

- *amount* - Withdraw amount.

