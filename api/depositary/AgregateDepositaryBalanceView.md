## AgregateDepositaryBalanceView





### Events
```solidity
DepositaryAdded(address depositary)
```

An event thats emitted when an new depositary added to agregate.



```solidity
DepositaryRemoved(address depositary)
```

An event thats emitted when an depositary removed from agregate.




### Variables
```solidity
uint256 maxSize
```

```solidity
uint256 decimals
```

```solidity
contract IDepositaryBalanceView[] depositaries
```

```solidity
mapping(address => uint256) depositariesIndex
```


### Functions
```solidity
constructor(uint256 _decimals, uint256 _maxSize)
```





**Arguments:**
- *_decimals* - Decimals balance.

- *_maxSize* - Max number depositaries in agregate.

```solidity
size() → uint256
```





**Returns:**
- *Depositaries* - count of agregate.

```solidity
addDepositary(address depositary)
```

Add depositary address to agregate.




**Arguments:**
- *depositary* - Added depositary address.

```solidity
removeDepositary(address depositary)
```

Removed depositary address from agregate.




**Arguments:**
- *depositary* - Removed depositary address.

```solidity
hasDepositary(address depositary) → bool
```





**Arguments:**
- *depositary* - Target depositary address.


**Returns:**
- *True* - if target depositary is allowed.

```solidity
allowedDepositaries() → address[]
```





**Returns:**
- *Allowed* - depositaries list.

```solidity
balance() → uint256
```





