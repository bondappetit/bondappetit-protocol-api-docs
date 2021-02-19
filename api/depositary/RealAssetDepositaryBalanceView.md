## RealAssetDepositaryBalanceView





### Events
```solidity
AssetUpdated(string id, uint256 updatedAt, struct RealAssetDepositaryBalanceView.Proof proof)
```

An event thats emitted when asset updated in portfolio.



```solidity
AssetRemoved(string id)
```

An event thats emitted when asset removed from portfolio.




### Variables
```solidity
uint256 maxSize
```

```solidity
uint256 decimals
```

```solidity
struct RealAssetDepositaryBalanceView.Asset[] portfolio
```

```solidity
mapping(string => uint256) portfolioIndex
```


### Functions
```solidity
constructor(uint256 _decimals, uint256 _maxSize)
```





**Arguments:**
- *_decimals* - Decimals balance.

- *_maxSize* - Max number assets in depositary.

```solidity
size() → uint256
```





**Returns:**
- *Assets* - count of depositary.

```solidity
assets() → struct RealAssetDepositaryBalanceView.Asset[]
```





**Returns:**
- *Assets* - list.

```solidity
put(string id, uint256 amount, uint256 price, uint256 updatedAt, string proofData, string proofSignature)
```

Update information of asset.




**Arguments:**
- *id* - Asset identificator.

- *amount* - Amount of asset.

- *price* - Cost of one asset in base currency.

- *updatedAt* - Timestamp of updated.

- *proofData* - Signed data.

- *proofSignature* - Data signature.

```solidity
remove(string id)
```

Remove information of asset.




**Arguments:**
- *id* - Asset identificator.

```solidity
balance() → uint256
```





