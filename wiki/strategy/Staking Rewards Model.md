# Staking Rewards Model

Sonr is a Cosmos powered blockchain which is powered by a TenderMint validation mechanism. The default consensus for TenderMint is DPoS and works with our current ABCI implementation for Transaction Verification. DPoS is a twist on Proof of Stake consensus that relies upon a group of delegates to validate blocks on behalf of all nodes in the network . Witnesses are elected by stakeholders at a rate of one vote per share per witness. Coin age is irrelevant. All coins that are mature will add the same staking weight (usually 1 in the wallet hover display) Results in stable, consistent interest only for active wallets and only with small inputs.

In the Sonr ecosystem, the process of staking involves two primary roles: Validators and Token Holders. Both roles are vital for the network's security, operation, and overall health. Here's how each role contributes and benefits from staking:

## **Validators: Network Gatekeepers**

Validators are the heart of the Sonr's Proof-of-Stake (PoS) mechanism. Their primary role is to validate and broadcast transactions to the network, propose new blocks in the blockchain, and ensure the overall integrity of the network's operations.

Validators are required to stake a significant amount of SNR tokens as a form of 'skin in the game.' This ensures they have a vested interest in properly maintaining the network. If they act maliciously or fail to efficiently perform their duties, they risk losing their staked tokens.

**Benefits for Validators:**

1. **Block Rewards**: Validators earn block rewards in the form of SNR tokens for each block they successfully propose and add to the blockchain.

2. **Transaction Fees**: Validators also earn a portion of the transaction fees from the transactions included in the blocks they propose.

3. **Influence**: Validators hold substantial influence within the network. The more SNR tokens a validator stakes, the higher the chances they have to propose the next block, thus increasing their potential earnings.

## **Token Holders: The Backbone of the Network**

Token holders are the individual or entities that own SNR tokens. They can participate in staking by delegating their tokens to validators. Delegation allows token holders to earn a portion of the validator's earnings, proportional to their stake, without needing to run a validator node themselves.

Token holders can choose which validator to delegate their tokens to based on factors like performance, commission rate, and reliability.

**Benefits for Token Holders:**

1. **Passive Earnings**: By delegating their tokens, token holders can earn passive income from the validator's block rewards and transaction fees.

2. **Governance**: Staking tokens often come with voting rights. Token holders can use their stakes to vote on governance proposals, influencing the direction of the Sonr network.

3. **Network Support**: By staking their tokens, token holders contribute to the overall security and stability of the Sonr network.

In summary, staking plays a crucial role in the Sonr ecosystem. Whether you're a validator running a node or a token holder contributing your tokens, staking brings benefits for all participants while ensuring the network's functionality and growth.

## **How to Stake Tokens**

If you are a token holder, you can support Sonr's network by staking your SNR tokens. Here's how it works and the benefits you can reap:

1. **Access your wallet**: Open your Sonr wallet where your SNR tokens are stored.

2. **Select the staking option**: Look for the staking or delegation section. Different wallets might use different terminologies.

3. **Choose the amount to stake**: Decide on the number of SNR tokens you want to stake. Keep in mind that staked tokens will be locked for a certain period and won't be available for transactions.

4. **Confirm your stake**: After reviewing all the details, confirm your stake. Your staked tokens are now helping secure and power the Sonr network.

**Benefits of Staking:**

Staking isn't just beneficial for Sonr's network; it's rewarding for stakeholders too. Here are the benefits:

1. **Earn rewards**: By staking your SNR tokens, you receive rewards over time. The more you stake and the longer the duration, the more rewards you accumulate.

2. **Participate in Governance**: Staking often comes with the right to vote on governance proposals. As a staker, you have a say in Sonr's future developments and decisions.

3. **Support the network**: By staking, you're providing stability and security to Sonr's network. You become an integral part of the ecosystem, supporting its growth and sustainability.

4. **Validator Incentives**: Validators are rewarded for their contributions to the network's security and reliability, encouraging responsible behavior and attracting high-quality validators.

**SonrStakingIncentives**

* **Staking Rewards**: Token holders can earn staking rewards by participating in securing the network, driving engagement and promoting long-term commitment.

* **Validator Incentives**: Validators are rewarded for their contributions to the network's security and reliability, encouraging responsible behavior and attracting high-quality validators.

**SonrDisincentives**

* **Slashing Penalties:**Validators who act maliciously or fail to maintain the network's integrity may face slashing penalties, discouraging bad behavior and ensuring overall network health.

* **Vesting Schedules:**Token allocations to team members and early investors follow a linear vesting schedule, discouraging short-term profit-taking and aligning interests with the long-term success of the Sonr ecosystem.

# Linear Vesting

Sonr's validators are subject to a linear vesting schedule, ensuring a gradual release of their rewards over time. This approach promotes long-term commitment and alignment of interests, contributing to the overall stability and security of the network. The clear path for the underlying application for staking is utilizing a Delegated Proof of Stake (DPoS) validation mechanism. Down the line Sonr will provide IPFS storage nodes, and governance participation in the staking model.

On Sonr we will be leveraging a**delegate stake**mechanism in order to**optimize buy-in**for users in the network. It imposes an**excess opportunity cost**if**slashing**is implemented.

**How Linear Vesting Works for Validators**

Upon successfully validating a block or transaction, validators earn a specific amount of SNR tokens as rewards. However, instead of immediately receiving the full reward, validators receive a fraction of their total rewards on a continuous basis over a defined vesting period.

For example, if a validator earns 1000 SNR tokens with a one-year vesting period, the validator will receive approximately 2.74 tokens every day (1000 tokens / 365 days) for a year, until the full reward is completely vested.

**Importance of Linear Vesting**

1. **Sustained Network Security**: By continuously vesting rewards, validators are incentivized to remain active and perform their duties diligently to continue receiving their rewards. This leads to a more secure and stable network.

2. **Long-term Commitment**: Linear vesting promotes a longer-term commitment from validators. This benefits the network by ensuring a consistent and dedicated set of validators, enhancing network reliability.

3. **Mitigation of Market Volatility**: By distributing the rewards over time, linear vesting can help mitigate the impact of large quantities of tokens entering the market at once, thus helping maintain token price stability.

**Why We Chose Linear Vesting**

The decision to implement linear vesting stems from our vision for Sonr as a robust and resilient network that prioritizes long-term sustainability over short-term gains. Linear vesting ensures that the validators are motivated to maintain a long-term involvement, thereby promoting a healthier, more committed validator set. It also helps to avoid sharp supply shocks, providing a more predictable token supply schedule, and hence, better stability for the SNR token.

