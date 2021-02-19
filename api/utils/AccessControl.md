## AccessControl





### Events
```solidity
AccessAllowed(address member)
```

An event emitted when address allowed.



```solidity
AccessDenied(address member)
```

An event emitted when address denied.




### Functions
```solidity
allowAccess(address member)
```

Allow access.




**Arguments:**
- *member* - Target address.

```solidity
denyAccess(address member)
```

Deny access.




**Arguments:**
- *member* - Target address.

```solidity
accessList() → address[]
```





**Returns:**
- *Allowed* - address list.

