## DepositaryUpdateValidator





### Events
```solidity
DepositaryUpdated(address newDepositary)
```

An event thats emitted when depositary address updated.



```solidity
BlockLimitUpdated(uint256 newBlockLimit)
```

An event thats emitted when block limit updated.




### Variables
```solidity
address depositary
```

```solidity
uint256 blockLimit
```


### Functions
```solidity
constructor(address _depositary, uint256 _blockLimit)
```





**Arguments:**
- *_depositary* - Depositary address.

- *_blockLimit* - Number of blocks from current.

```solidity
changeDepositary(address _depositary)
```

Update depositary address.




**Arguments:**
- *_depositary* - New depositary address.

```solidity
changeBlockLimit(uint256 _blockLimit)
```

Update block limit.




**Arguments:**
- *_blockLimit* - New block limit.

```solidity
validate() → bool
```





