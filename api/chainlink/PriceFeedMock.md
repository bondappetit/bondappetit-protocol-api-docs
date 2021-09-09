## PriceFeedMock





### Variables
```solidity
uint8 decimals
```

```solidity
uint256 version
```

```solidity
mapping(uint80 => struct PriceFeedMock.Round) _rounds
```

```solidity
uint80 latestRoundId
```


### Functions
```solidity
constructor(uint8 _decimals, uint256 _version)
```





```solidity
addRound(uint80 roundId, int256 answer, uint256 startedAt, uint256 updatedAt, uint80 answeredInRound)
```





```solidity
getRoundData(uint80 _roundId) → uint80 roundId, int256 answer, uint256 startedAt, uint256 updatedAt, uint80 answeredInRound
```





```solidity
latestRoundData() → uint80 roundId, int256 answer, uint256 startedAt, uint256 updatedAt, uint80 answeredInRound
```





