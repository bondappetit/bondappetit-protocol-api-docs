## Vesting





### Events
```solidity
DelegateVotes(address delegatee)
```

An event emitted when all votes delegate to.



```solidity
Locked(uint256 periodId)
```

An event emitted when locking a period.



```solidity
Revoked(uint256 periodId)
```

An event emitted when revoked a period.



```solidity
Withdrawal(address recipient, uint256 periodId)
```

An event emitted when withdrawal a period.




### Variables
```solidity
contract ERC20 token
```

```solidity
uint256 currentPeriod
```

```solidity
struct EnumerableSet.AddressSet participants
```

```solidity
mapping(address => mapping(uint256 => struct Vesting.Period)) periods
```

```solidity
mapping(address => uint256[]) periodsIndex
```


### Functions
```solidity
maxPeriodsPerRecipient() → uint256
```

The number of periods for a per recipient.



```solidity
constructor(address _token)
```





**Arguments:**
- *_token* - Address of vesting token contract.

```solidity
delegate(address governanceToken, address delegatee)
```

Delegate votes to delegatee.




**Arguments:**
- *delegatee* - The address to delegate votes to

```solidity
lock(address recipient, uint256 amount, string description, uint256 date) → uint256
```

Add new period.




**Arguments:**
- *recipient* - Recipient of reward.

- *amount* - Reward amount.

- *date* - Date of unlockd period.


**Returns:**
- *Added* - period identifier.

```solidity
revoke(address recipient, uint256 periodId)
```

Revoke period.




**Arguments:**
- *recipient* - Recipient of reward.

- *periodId* - Period identifier.

```solidity
getParticipants() → address[]
```

Return all participants addresses.




**Returns:**
- *Participants* - addresses.

```solidity
info(address recipient) → struct Vesting.Period[]
```

Get information of period.




**Arguments:**
- *recipient* - Recipient address.


**Returns:**
- *Recipient* - periods list.

```solidity
withdraw(uint256 periodId)
```

Withdraw reward.




**Arguments:**
- *periodId* - Target period identifier.

