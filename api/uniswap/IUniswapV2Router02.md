## IUniswapV2Router02





### Functions
```solidity
factory() → address
```





```solidity
WETH() → address
```





```solidity
addLiquidity(address tokenA, address tokenB, uint256 amountADesired, uint256 amountBDesired, uint256 amountAMin, uint256 amountBMin, address to, uint256 deadline) → uint256 amountA, uint256 amountB, uint256 liquidity
```





```solidity
addLiquidityETH(address token, uint256 amountTokenDesired, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline) → uint256 amountToken, uint256 amountETH, uint256 liquidity
```





```solidity
removeLiquidity(address tokenA, address tokenB, uint256 liquidity, uint256 amountAMin, uint256 amountBMin, address to, uint256 deadline) → uint256 amountA, uint256 amountB
```





```solidity
removeLiquidityETH(address token, uint256 liquidity, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline) → uint256 amountToken, uint256 amountETH
```





```solidity
removeLiquidityWithPermit(address tokenA, address tokenB, uint256 liquidity, uint256 amountAMin, uint256 amountBMin, address to, uint256 deadline, bool approveMax, uint8 v, bytes32 r, bytes32 s) → uint256 amountA, uint256 amountB
```





```solidity
removeLiquidityETHWithPermit(address token, uint256 liquidity, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline, bool approveMax, uint8 v, bytes32 r, bytes32 s) → uint256 amountToken, uint256 amountETH
```





```solidity
swapExactTokensForTokens(uint256 amountIn, uint256 amountOutMin, address[] path, address to, uint256 deadline) → uint256[] amounts
```





```solidity
swapTokensForExactTokens(uint256 amountOut, uint256 amountInMax, address[] path, address to, uint256 deadline) → uint256[] amounts
```





```solidity
swapExactETHForTokens(uint256 amountOutMin, address[] path, address to, uint256 deadline) → uint256[] amounts
```





```solidity
swapTokensForExactETH(uint256 amountOut, uint256 amountInMax, address[] path, address to, uint256 deadline) → uint256[] amounts
```





```solidity
swapExactTokensForETH(uint256 amountIn, uint256 amountOutMin, address[] path, address to, uint256 deadline) → uint256[] amounts
```





```solidity
swapETHForExactTokens(uint256 amountOut, address[] path, address to, uint256 deadline) → uint256[] amounts
```





```solidity
quote(uint256 amountA, uint256 reserveA, uint256 reserveB) → uint256 amountB
```





```solidity
getAmountOut(uint256 amountIn, uint256 reserveIn, uint256 reserveOut) → uint256 amountOut
```





```solidity
getAmountIn(uint256 amountOut, uint256 reserveIn, uint256 reserveOut) → uint256 amountIn
```





```solidity
getAmountsOut(uint256 amountIn, address[] path) → uint256[] amounts
```





```solidity
getAmountsIn(uint256 amountOut, address[] path) → uint256[] amounts
```





```solidity
removeLiquidityETHSupportingFeeOnTransferTokens(address token, uint256 liquidity, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline) → uint256 amountETH
```





```solidity
removeLiquidityETHWithPermitSupportingFeeOnTransferTokens(address token, uint256 liquidity, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline, bool approveMax, uint8 v, bytes32 r, bytes32 s) → uint256 amountETH
```





```solidity
swapExactTokensForTokensSupportingFeeOnTransferTokens(uint256 amountIn, uint256 amountOutMin, address[] path, address to, uint256 deadline)
```





```solidity
swapExactETHForTokensSupportingFeeOnTransferTokens(uint256 amountOutMin, address[] path, address to, uint256 deadline)
```





```solidity
swapExactTokensForETHSupportingFeeOnTransferTokens(uint256 amountIn, uint256 amountOutMin, address[] path, address to, uint256 deadline)
```





