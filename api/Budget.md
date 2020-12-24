## Budget





### Events
```solidity
ExpenditureChanged(address recipient, uint256 min, uint256 target)
```

An event emitted when expenditure item changed.



```solidity
Payed(address recipient, uint256 amount)
```

An event emitted when expenditure item payed.




### Variables
```solidity
mapping(address => struct Budget.Expenditure) expenditures
```

```solidity
struct EnumerableSet.AddressSet recipients
```


### Functions
```solidity
receive()
```





```solidity
changeExpenditure(address recipient, uint256 min, uint256 target)
```

Change expenditure item.




**Arguments:**
- *recipient* - Recipient address.

- *min* - Minimal balance for payment.

- *target* - Target balance.

```solidity
transferETH(address payable recipient, uint256 amount) → bool
```

Transfer ETH to recipient.




**Arguments:**
- *recipient* - Recipient.

- *amount* - Transfer amount.

```solidity
getRecipients() → address[]
```

Return all recipients addresses.




**Returns:**
- *Recipients* - addresses.

```solidity
deficitTo(address recipient) → uint256
```

Return balance deficit of recipient.




**Arguments:**
- *recipient* - Target recipient.


**Returns:**
- *Balance* - deficit of recipient.

```solidity
deficit() → uint256
```

Return summary balance deficit of all recipients.




**Returns:**
- *Summary* - balance deficit of all recipients.

```solidity
pay()
```

Pay ETH to all recipients with balance deficit.



