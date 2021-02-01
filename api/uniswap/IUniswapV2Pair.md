## IUniswapV2Pair





### Events
```solidity
Approval(address owner, address spender, uint256 value)
```





```solidity
Transfer(address from, address to, uint256 value)
```





```solidity
Mint(address sender, uint256 amount0, uint256 amount1)
```





```solidity
Burn(address sender, uint256 amount0, uint256 amount1, address to)
```





```solidity
Swap(address sender, uint256 amount0In, uint256 amount1In, uint256 amount0Out, uint256 amount1Out, address to)
```





```solidity
Sync(uint112 reserve0, uint112 reserve1)
```






### Variables

### Functions
```solidity
name() → string
```





```solidity
symbol() → string
```





```solidity
decimals() → uint8
```





```solidity
totalSupply() → uint256
```





```solidity
balanceOf(address owner) → uint256
```





```solidity
allowance(address owner, address spender) → uint256
```





```solidity
approve(address spender, uint256 value) → bool
```





```solidity
transfer(address to, uint256 value) → bool
```





```solidity
transferFrom(address from, address to, uint256 value) → bool
```





```solidity
DOMAIN_SEPARATOR() → bytes32
```





```solidity
PERMIT_TYPEHASH() → bytes32
```





```solidity
nonces(address owner) → uint256
```





```solidity
permit(address owner, address spender, uint256 value, uint256 deadline, uint8 v, bytes32 r, bytes32 s)
```





```solidity
MINIMUM_LIQUIDITY() → uint256
```





```solidity
factory() → address
```





```solidity
token0() → address
```





```solidity
token1() → address
```





```solidity
getReserves() → uint112 reserve0, uint112 reserve1, uint32 blockTimestampLast
```





```solidity
price0CumulativeLast() → uint256
```





```solidity
price1CumulativeLast() → uint256
```





```solidity
kLast() → uint256
```





```solidity
mint(address to) → uint256 liquidity
```





```solidity
burn(address to) → uint256 amount0, uint256 amount1
```





```solidity
swap(uint256 amount0Out, uint256 amount1Out, address to, bytes data)
```





```solidity
skim(address to)
```





```solidity
sync()
```





```solidity
initialize(address, address)
```





