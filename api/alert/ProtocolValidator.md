## ProtocolValidator





### Events
```solidity
ProtocolContractAdded(address newContract)
```

An event thats emitted when protocol contract added.



```solidity
ProtocolContractRemoved(address removedContract)
```

An event thats emitted when protocol contract removed.



```solidity
ValidatorAdded(address validator, address controlledContract)
```

An event thats emitted when validator added.



```solidity
ValidatorRemoved(address validator)
```

An event thats emitted when validator removed.



```solidity
InvalidState(address validator, address controlledContract)
```

An event thats emitted when state invalid.




### Variables
```solidity
uint256 maxSize
```

```solidity
struct EnumerableSet.AddressSet protocolContracts
```

```solidity
mapping(address => address) validators
```

```solidity
struct EnumerableSet.AddressSet validatorsIndex
```


### Functions
```solidity
constructor(uint256 _maxSize)
```





**Arguments:**
- *_maxSize* - Maximal count of protocol contracts and validators.

```solidity
size() → uint256
```





**Returns:**
- *Validators* - count of agregate.

```solidity
addProtocolContract(address _contract)
```





**Arguments:**
- *_contract* - Protocol contract address.

```solidity
removeProtocolContract(address _contract)
```





**Arguments:**
- *_contract* - Protocol contract address.

```solidity
protocolContractsList() → address[]
```





**Returns:**
- *Addresses* - of all protocol contracts.

```solidity
addValidator(address validator, address controlledContract)
```





**Arguments:**
- *validator* - Validator address.

- *controlledContract* - Pausable contract address (zero address for all protocol contracts).

```solidity
removeValidator(address validator)
```





**Arguments:**
- *validator* - Validator address.

```solidity
validatorsList() → address[]
```





**Returns:**
- *Validators* - addresses list.

```solidity
validate(address validator) → bool
```

Validate protocol state and pause controlled contract if state invalid.




**Arguments:**
- *validator* - Target validator.


**Returns:**
- *Is* - state valid.

