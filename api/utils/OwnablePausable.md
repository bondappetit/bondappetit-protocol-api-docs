## OwnablePausable





### Events
```solidity
PauserChanged(address newPauser)
```

An event thats emitted when an pauser address changed.




### Variables
```solidity
address pauser
```


### Functions
```solidity
changePauser(address newPauser)
```

Change pauser account.




**Arguments:**
- *newPauser* - Address of new pauser account.

```solidity
pause()
```

Triggers stopped state.



```solidity
unpause()
```

Returns to normal state.



