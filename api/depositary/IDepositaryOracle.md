## IDepositaryOracle





### Events
```solidity
Update(string isin, uint256 amount)
```



Emitted when the depositary update.


### Variables

### Functions
```solidity
put(string isin, uint256 amount)
```

Write a security amount to the storage mapping.




**Arguments:**
- *isin* - International securities identification number.

- *amount* - Amount of securities.

```solidity
get(string isin) → struct IDepositaryOracle.Security
```

Get amount securities.




**Arguments:**
- *isin* - International securities identification number.


**Returns:**
- *amount* - Amount of securities.

```solidity
all() → struct IDepositaryOracle.Security[]
```

Get all depositary securities.




**Returns:**
- *All* - securities.

