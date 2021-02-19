## VestingSplitter





### Events
```solidity
SharesChanged()
```

An event emitted when shares changed.



```solidity
VestingWithdraw(address vesting, uint256 periodId)
```

An event emitted when vesting period withdrawal.



```solidity
Split(address token)
```

An event emitted when split a balance.



```solidity
Withdraw(address token, address account, uint256 reward)
```

An event emitted when withdrawal a token.




### Variables
```solidity
mapping(address => uint256) totalSupply
```

```solidity
mapping(address => mapping(address => uint256)) _balances
```

```solidity
address[] _accounts
```

```solidity
mapping(address => uint256) _share
```


### Functions
```solidity
getMaxAccounts() → uint256
```

Get accounts limit for split.




**Returns:**
- *Max* - accounts for split.

```solidity
getAccounts() → address[]
```

Get accounts with share list.




**Returns:**
- *Addresses* - of all accounts with share.

```solidity
balanceOf(address token, address account) → uint256
```

Get balance of account.




**Arguments:**
- *token* - Target token.

- *account* - Target account.


**Returns:**
- *Balance* - of account.

```solidity
shareOf(address account) → uint256
```

Get share of account in split.




**Arguments:**
- *account* - Target account.


**Returns:**
- *Share* - in split.

```solidity
changeShares(address[] accounts, uint256[] shares)
```

Change shares of accounts in split.




**Arguments:**
- *accounts* - Accounts list.

- *shares* - Shares in split.

```solidity
vestingWithdraw(contract Vesting vesting, uint256 periodId)
```

Withdraw reward from vesting contract.




**Arguments:**
- *vesting* - Address of vesting contract.

- *periodId* - Target vesting period.

```solidity
split(address token)
```

Split token to all accounts.




**Arguments:**
- *token* - Target token.

```solidity
withdraw(address token)
```

Withdraw token balance to sender.




**Arguments:**
- *token* - Target token.

