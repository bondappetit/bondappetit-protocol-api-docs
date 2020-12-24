## GovernorAlpha





### Events
```solidity
ProposalCreated(uint256 id, address proposer, address[] targets, uint256[] values, string[] signatures, bytes[] calldatas, uint256 startBlock, uint256 endBlock, string description)
```

An event emitted when a new proposal is created



```solidity
VoteCast(address voter, uint256 proposalId, bool support, uint256 votes)
```

An event emitted when a vote has been cast on a proposal



```solidity
ProposalCanceled(uint256 id)
```

An event emitted when a proposal has been canceled



```solidity
ProposalQueued(uint256 id, uint256 eta)
```

An event emitted when a proposal has been queued in the Timelock



```solidity
ProposalExecuted(uint256 id)
```

An event emitted when a proposal has been executed in the Timelock




### Variables
```solidity
string name
```

```solidity
contract TimelockInterface timelock
```

```solidity
contract BondInterface bond
```

```solidity
address guardian
```

```solidity
uint256 proposalCount
```

```solidity
mapping(uint256 => struct GovernorAlpha.Proposal) proposals
```

```solidity
mapping(address => uint256) latestProposalIds
```

```solidity
bytes32 DOMAIN_TYPEHASH
```

```solidity
bytes32 BALLOT_TYPEHASH
```


### Functions
```solidity
quorumVotes() → uint256
```

The number of votes in support of a proposal required in order for a quorum to be reached and for a vote to succeed



```solidity
proposalThreshold() → uint256
```

The number of votes required in order for a voter to become a proposer



```solidity
proposalMaxOperations() → uint256
```

The maximum number of actions that can be included in a proposal



```solidity
votingDelay() → uint256
```

The delay before voting on a proposal may take place, once proposed



```solidity
votingPeriod() → uint256
```

The duration of voting on a proposal, in blocks



```solidity
constructor(address timelock_, address bond_, address guardian_)
```





```solidity
propose(address[] targets, uint256[] values, string[] signatures, bytes[] calldatas, string description) → uint256
```





```solidity
queue(uint256 proposalId)
```





```solidity
execute(uint256 proposalId)
```





```solidity
cancel(uint256 proposalId)
```





```solidity
getActions(uint256 proposalId) → address[] targets, uint256[] values, string[] signatures, bytes[] calldatas
```





```solidity
getReceipt(uint256 proposalId, address voter) → struct GovernorAlpha.Receipt
```





```solidity
state(uint256 proposalId) → enum GovernorAlpha.ProposalState
```





```solidity
castVote(uint256 proposalId, bool support)
```





```solidity
castVoteBySig(uint256 proposalId, bool support, uint8 v, bytes32 r, bytes32 s)
```





```solidity
__acceptAdmin()
```





```solidity
__abdicate()
```





```solidity
__queueSetTimelockPendingAdmin(address newPendingAdmin, uint256 eta)
```





```solidity
__executeSetTimelockPendingAdmin(address newPendingAdmin, uint256 eta)
```





