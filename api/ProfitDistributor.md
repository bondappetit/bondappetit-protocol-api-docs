## ProfitDistributor





### Events
```solidity
RewardAdded(uint256 reward)
```

An event thats emitted when an reward token addet to contract.



```solidity
Staked(address user, uint256 amount)
```

An event thats emitted when an staking token added to contract.



```solidity
Withdrawn(address user, uint256 amount)
```

An event thats emitted when an staking token withdrawal from contract.



```solidity
RewardPaid(address user, uint256 reward)
```

An event thats emitted when an reward token withdrawal from contract.



```solidity
RewardsDistributionChanged(address newRewardsDistribution)
```

An event thats emitted when an rewards distribution address changed.



```solidity
RewardsTransfered(address recipient, uint256 amount)
```

An event thats emitted when an rewards tokens transfered to recipient.




### Variables
```solidity
address rewardsDistribution
```

```solidity
contract IERC20 rewardsToken
```

```solidity
contract IERC20 stakingToken
```

```solidity
uint256 periodFinish
```

```solidity
uint256 rewardRate
```

```solidity
uint256 rewardsDuration
```

```solidity
uint256 lastUpdateBlock
```

```solidity
uint256 rewardPerTokenStored
```

```solidity
uint256 lockPeriod
```

```solidity
uint256 unlockPeriod
```

```solidity
mapping(address => uint256) userRewardPerTokenPaid
```

```solidity
mapping(address => uint256) rewards
```

```solidity
uint256 _totalSupply
```

```solidity
mapping(address => uint256) _balances
```

```solidity
mapping(address => uint256) _stakeAt
```

```solidity
mapping(address => uint256) _penaltyAmount
```


### Functions
```solidity
constructor(address _rewardsDistribution, uint256 _rewardsDuration, address _rewardsToken, address _stakingToken, uint256 _lockPeriod, uint256 _unlockPeriod)
```





**Arguments:**
- *_rewardsDistribution* - Rewards distribution address.

- *_rewardsDuration* - Duration of distribution.

- *_rewardsToken* - Address of reward token.

- *_stakingToken* - Address of staking token.

- *_lockPeriod* - Stake lock period.

- *_unlockPeriod* - Stake unlock period.

```solidity
totalSupply() → uint256
```





**Returns:**
- *Total* - staking token amount.

```solidity
balanceOf(address account) → uint256
```





**Arguments:**
- *account* - Target account.


**Returns:**
- *Staking* - token amount.

```solidity
lockInfo(address account) → bool locked, uint256 mod, uint256 nextUnlock, uint256 nextLock, uint256 stakeAt
```





```solidity
lastTimeRewardApplicable() → uint256
```





**Returns:**
- *Block* - number of last reward.

```solidity
rewardPerToken() → uint256
```





**Returns:**
- *Reward* - per token.

```solidity
earned(address account) → uint256
```





**Arguments:**
- *account* - Target account.


**Returns:**
- *Earned* - rewards.

```solidity
penalty(address account) → uint256
```





**Arguments:**
- *account* - Target account.


**Returns:**
- *Penalty* - rewards.

```solidity
getRewardForDuration() → uint256
```





**Returns:**
- *Rewards* - amount for duration.

```solidity
stake(uint256 amount)
```

Stake token.




**Arguments:**
- *amount* - Amount staking token.

```solidity
getReward()
```

Withdraw reward token.



```solidity
exit()
```

Withdraw reward and staking token.



```solidity
changeRewardsDistribution(address _rewardDistribution)
```

Change rewards distribution address.




**Arguments:**
- *_rewardDistribution* - New rewards distribution address.

```solidity
notifyRewardAmount(uint256 reward)
```

Start distribution.




**Arguments:**
- *reward* - Distributed rewards amount.

