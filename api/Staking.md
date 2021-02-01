## Staking





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



```solidity
StakingEndBlockChanged(uint256 newBlockNumber)
```

An event thats emitted when an staking end block number changed.



```solidity
UnstakingStartBlockChanged(uint256 newBlockNumber)
```

An event thats emitted when an unstaking start block number changed.




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
uint256 stakingEndBlock
```

```solidity
uint256 unstakingStartBlock
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


### Functions
```solidity
constructor(address _rewardsDistribution, uint256 _rewardsDuration, address _rewardsToken, address _stakingToken, uint256 _stakingEndBlock, uint256 _unstakingStartBlock)
```





**Arguments:**
- *_rewardsDistribution* - Rewards distribution address.

- *_rewardsDuration* - Duration of distribution.

- *_rewardsToken* - Address of reward token.

- *_stakingToken* - Address of staking token.

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
withdraw(uint256 amount)
```

Withdraw staking token.




**Arguments:**
- *amount* - Amount withdraw token.

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
transfer(address recipient, uint256 amount)
```

Transfer rewards token to recipient if distribution not start.




**Arguments:**
- *recipient* - Recipient.

- *amount* - Amount transfered rewards token.

```solidity
changeStakingEndBlock(uint256 _stakingEndBlock)
```

Change staking end block number.




**Arguments:**
- *_stakingEndBlock* - New staking end block number.

```solidity
changeUnstakingStartBlock(uint256 _unstakingStartBlock)
```

Change unstaking start block number.




**Arguments:**
- *_unstakingStartBlock* - New unstaking start block number.

```solidity
notifyRewardAmount(uint256 reward)
```

Start distribution.




**Arguments:**
- *reward* - Distributed rewards amount.

