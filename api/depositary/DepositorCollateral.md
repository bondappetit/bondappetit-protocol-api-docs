## DepositorCollateral





### Events
```solidity
Lock(address token, address depositor, uint256 amount)
```

An event emitted when collateral locked.



```solidity
Withdraw(address token, address depositor, uint256 amount)
```

An event emitted when collateral withdraw.




### Variables
```solidity
uint256 maxSize
```

```solidity
mapping(address => uint256) totalSupply
```

```solidity
mapping(address => struct EnumerableSet.AddressSet) _depositors
```

```solidity
mapping(address => mapping(address => uint256)) _balances
```


### Functions
```solidity
constructor(uint256 _maxSize)
```





**Arguments:**
- *_maxSize* - Max number of depositors.

```solidity
getDepositors(address token) → address[]
```

Get depositors.




**Arguments:**
- *token* - Collateral token.


**Returns:**
- *Addresses* - of all depositors.

```solidity
balanceOf(address token, address depositor) → uint256
```

Get balance of depositor.




**Arguments:**
- *token* - Target token.

- *depositor* - Target depositor.


**Returns:**
- *Balance* - of depositor.

```solidity
lock(address token, address depositor, uint256 amount)
```

Lock depositor collateral.




**Arguments:**
- *token* - Locked token.

- *depositor* - Depositor address.

- *amount* - Locked amount.

```solidity
withdraw(address token, address depositor, uint256 amount)
```

Withdraw depositor collateral.




**Arguments:**
- *token* - Withdraw token.

- *depositor* - Depositor address.

- *amount* - Withdraw amount.

