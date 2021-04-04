## ISecurityOracle





### Events
```solidity
Update(string isin, string prop, bytes value)
```



Emitted when the security property update.


### Variables

### Functions
```solidity
put(string isin, string prop, bytes value)
```

Put property value of security.




**Arguments:**
- *isin* - International securities identification number of security.

- *prop* - Property name of security.

- *value* - Property value.

```solidity
get(string isin, string prop) → bytes
```

Get property value of security.




**Arguments:**
- *isin* - International securities identification number of security.

- *prop* - Property name of security.


**Returns:**
- *Property* - value of security.

