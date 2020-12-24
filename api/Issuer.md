## Issuer





### Events
```solidity
TransferTreasury(address newTreasury)
```

An event thats emitted when an Treasury contract transfered.



```solidity
Rebalance()
```

An event thats emitted when an ABT total supply rebalanced.




### Variables
```solidity
contract ABT abt
```

```solidity
address treasury
```


### Functions
```solidity
constructor(address _abt, address _treasury)
```





**Arguments:**
- *_abt* - ABT contract address.

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

Rebalance ABT total supply by depositary balance. Mint ABT tokens if depositary balance greater token total supply and burn otherwise.



