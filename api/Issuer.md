## Issuer





### Events
```solidity
TransferTreasury(address newTreasury)
```

An event thats emitted when an Treasury contract transfered.



```solidity
Rebalance()
```

An event thats emitted when an stable token total supply rebalanced.




### Variables
```solidity
contract StableToken stableToken
```

```solidity
address treasury
```


### Functions
```solidity
constructor(address _stableToken, address _treasury)
```





**Arguments:**
- *_stableToken* - Stable token contract address.

- *_treasury* - Treasury contract address.

```solidity
changeTreasury(address _treasury)
```

Transfer Treasury contract to new address.




**Arguments:**
- *_treasury* - New address Treasury contract.

```solidity
rebalance()
```

Rebalance stable token total supply by depositary balance. Mint stable token if depositary balance greater token total supply and burn otherwise.



