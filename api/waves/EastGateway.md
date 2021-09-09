## EastGateway





### Events
```solidity
Buy(address customer, address currency, uint256 sell, uint256 buy, uint256 reward)
```

An event thats emitted when an account buyed token.




### Variables
```solidity
contract Market market
```

```solidity
address recipient
```


### Functions
```solidity
constructor(address _market, address _recipient)
```





```solidity
buy(contract ERC20 currency, uint256 amount) → bool
```





