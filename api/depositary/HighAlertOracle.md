## HighAlertOracle





### Events
```solidity
ContractAdded(address addedContract)
```

An event emitted when contract added to pausable list.



```solidity
ContractRemoved(address removedContract)
```

An event emitted when contract removed at pausable list.



```solidity
PausedAll(string reason)
```

An event emitted when paused all contracts.



```solidity
UnpausedAll(string reason)
```

An event emitted when unpaused all contracts.




### Variables

### Functions
```solidity
addContract(address _contract)
```

Add contract to pausable list.




**Arguments:**
- *_contract* - Target contract.

```solidity
removeContract(address _contract)
```

Remove contract at pausable list.




**Arguments:**
- *_contract* - Target contract.

```solidity
getContracts() → address[]
```

Return all pausable contracts.




**Returns:**
- *Pausable* - contracts list.

```solidity
pauseAll(string reason)
```

Pause all pausable contracts.




**Arguments:**
- *reason* - Reason of pause.

```solidity
unpauseAll(string reason)
```

Unpause all pausable contracts.




**Arguments:**
- *reason* - Reason of unpause.

