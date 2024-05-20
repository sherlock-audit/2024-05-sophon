
# Sophon contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
Ethereum
___

### Q: If you are integrating tokens, are you allowing only whitelisted tokens to work with the codebase or any complying with the standard? Are they assumed to have certain properties, e.g. be non-reentrant? Are there any types of <a href="https://github.com/d-xo/weird-erc20" target="_blank" rel="noopener noreferrer">weird tokens</a> you want to integrate?
Only whitelisted ERC20 standard tokens can work with the codebase.
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED? If these integrations are trusted, should auditors also assume they are always responsive, for example, are oracles trusted to provide non-stale information, or VRF providers to respond within a designated timeframe?
All the external admins are trusted. 
___

### Q: Are there any protocol roles? Please list them and provide whether they are TRUSTED or RESTRICTED, or provide a more comprehensive description of what a role can and can't do/impact.
There is a single admin (owner) that is trusted.
___

### Q: For permissioned functions, please list all checks and requirements that will be made before calling the function.
Permissioned functions are secure by OZ Ownable (onlyOwner modifier).
___

### Q: Is the codebase expected to comply with any EIPs? Can there be/are there any deviations from the specification?
n/a
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, arbitrage bots, etc.)?
no
___

### Q: Are there any hardcoded values that you intend to change before (some) deployments?
Yes. The specifics around per block points emission rate for the farm as a whole and for each pool will be defined later. The specific pools in the farm will be finalized later as well.
___

### Q: If the codebase is to be deployed on an L2, what should be the behavior of the protocol in case of sequencer issues (if applicable)? Should Sherlock assume that the Sequencer won't misbehave, including going offline?
We only plan to deploy the codebase on Ethereum mainnet at this time.
___

### Q: Should potential issues, like broken assumptions about function behavior, be reported if they could pose risks in future integrations, even if they might not be an issue in the context of the scope? If yes, can you elaborate on properties/invariants that should hold?
n/a
___

### Q: Please discuss any design choices you made.
n/a
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
n/a
___

### Q: We will report issues where the core protocol functionality is inaccessible for at least 7 days. Would you like to override this value?
no need to override
___

### Q: Please provide links to previous audits (if any).
n/a
___

### Q: Please list any relevant protocol resources.
https://docs.sophon.xyz/

___

### Q: Additional audit information.
Any bridging related code is considered out of scope
___



# Audit scope


[farming-contracts @ c08a2a81f2d5359bc05f41a25df54c7a91a73a03](https://github.com/sophon-org/farming-contracts/tree/c08a2a81f2d5359bc05f41a25df54c7a91a73a03)
- [farming-contracts/contracts/farm/SophonFarming.sol](farming-contracts/contracts/farm/SophonFarming.sol)
- [farming-contracts/contracts/farm/SophonFarmingState.sol](farming-contracts/contracts/farm/SophonFarmingState.sol)
- [farming-contracts/contracts/proxies/Proxy2Step.sol](farming-contracts/contracts/proxies/Proxy2Step.sol)
- [farming-contracts/contracts/proxies/SophonFarmingProxy.sol](farming-contracts/contracts/proxies/SophonFarmingProxy.sol)
- [farming-contracts/contracts/proxies/Upgradeable2Step.sol](farming-contracts/contracts/proxies/Upgradeable2Step.sol)

