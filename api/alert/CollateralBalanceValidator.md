## CollateralBalanceValidator





### Events
```solidity
StableTokenUpdated(address newStableToken)
```

An event thats emitted when stable token address updated.



```solidity
CollateralUpdated(address newCollateral)
```

An event thats emitted when collateral address updated.



```solidity
PermissibleImbalanceUpdated(uint256 newPermissibleImbalance)
```

An event thats emitted when permissible imbalance updated.




### Variables
```solidity
uint256 PERMISSIBLE_DECIMALS
```

```solidity
contract ERC20 stableToken
```

```solidity
contract IDepositaryBalanceView collateral
```

```solidity
uint256 permissibleImbalance
```


### Functions
```solidity
constructor(address _stableToken, address _collateral, uint256 _permissibleImbalance)
```





**Arguments:**
- *_stableToken* - Address of stable token.

- *_collateral* - Address of collateral.

- *_permissibleImbalance* - Permissible imbalance of stable token total supply and collateral balance.

```solidity
changeStableToken(address _stableToken)
```





**Arguments:**
- *_stableToken* - New stable token address.

```solidity
changeCollateral(address _collateral)
```





**Arguments:**
- *_collateral* - New collateral address.

```solidity
changePermissibleImbalance(uint256 _permissibleImbalance)
```





**Arguments:**
- *_permissibleImbalance* - New permissible imbalance value.

```solidity
validate() → bool
```





