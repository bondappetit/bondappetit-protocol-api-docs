## IOneSplit





### Functions
```solidity
getExpectedReturn(contract IERC20 fromToken, contract IERC20 destToken, uint256 amount, uint256 parts, uint256 flags) → uint256 returnAmount, uint256[] distribution
```





```solidity
getExpectedReturnWithGas(contract IERC20 fromToken, contract IERC20 destToken, uint256 amount, uint256 parts, uint256 flags, uint256 destTokenEthPriceTimesGasPrice) → uint256 returnAmount, uint256 estimateGasAmount, uint256[] distribution
```





```solidity
swap(contract IERC20 fromToken, contract IERC20 destToken, uint256 amount, uint256 minReturn, uint256[] distribution, uint256 flags) → uint256 returnAmount
```





