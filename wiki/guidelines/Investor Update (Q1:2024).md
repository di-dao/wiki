# Investor Update - Q1/2024

**Dear Valued Stakeholders,**



As many of you know we had a rocky end to 2022 which led to a quietly productive 2023 where we participated in the [Paris POT conference](https://venturebeat.com/business/proof-of-talk-2023-has-just-closed-the-first-round-of-its-start-up-competition/), optimized Sonr’s MPC Algorithm to be [240x faster](https://www.sonr.io/blog/engineering/optimizing-mpc), and conducted research which allowed us to uncover that a single Sonr Node would be able to handle 33,000X the load that Google Servers handle a second due to DID Authentication. This should be a brief refresher on old news as the real purpose of this email is to bring some exciting updates regarding our Public TestNet.

***

# Sonr’s Mission

Before I go over our latest changes, I want to quickly reiterate Sonr’s mission and values. We’ve always been focused on delivering secure, self-sovereign experiences which empower the end-user. We do this by capitalizing on decentralized technology to maximize marketplace network effects for our developers. This mission led us to focus on isolating our goals of: Platform Interoperability, Regulatory compliance, and transitioning familiar user experience to a Web3 Environment. I say all this to make it clear that the [development of Sonr is a long continuous block](https://www.youtube.com/watch?v=bex88Ku9Crk\&t=1s) of three years of iterative research and development which allowed us to build intuition for the identity market. 

***

# A Light at the End of the Tunnel

![](assets/Y-zbLjrarPkDsaih49-qWO5TzHLP75iXFft8PSg6OyM=.blob)

With that all being said our industry has received a far greater amount of clarity with the Bitcoin ETF now being passed, and Cosmos SDK based blockchains have been [outperforming the Altcoin market](https://crypto.com/price/categories/cosmos-ecosystem). With plans to launch Mainnet within the next month, and our resources raised from fundraising 26 months ago mostly exhausted its critical that we position Sonr in a “Stable Launchpad” prior to commencing the “Rocket Launch”.

***

# “The Holy Public Testnet”

We officially became*“Significantly Decentralized”*. Meaning, we reached the point where optimizations made to the codebase to further decentralize the system — would no longer offer additional security or benefit to the underlying validator node. In practical terms, we see this where validator stakes become slashed when failing to decrypt sensitive user key information.

###### 🔒 **Sonr is not a traditional wallet, social profile, or chat service. Sonr is a fresh new take on Decentralized Identity which uses the “Highway” p2p network. Our priority is making it clear to users that Sonr is anonymous, self-sovereign identity AppChain.**

1. Users contribute Social (Github, Twitter, etc.) and Personal (Phone, Email, Etc.) identifiers which are “accumulated” with Zero Knowledge proofs to anonymously provide authenticity to their Sonr Identities. This also creates the feature where Sonr Identities can verify ownership of identifiers with a simple Blockchain Query.

2. After using [capsule](https://usecapsule.com/) and the [family wallet app](https://family.co/) to get a gist of the current state of Web3 User Experience, I learned we needed to capitalize on the latest advancements in Frontend Engineering to stay agile and outpace the development of the existing market. As many of you know ***Sonr introduced the first “embeddable wallet” back in 2022*** with our Flutter client.

3. After keeping a closer watch on the [HTMX Project](https://htmx.org/), we were able to skip the “embeddable” step entirely and introduce a “Validator Proxied Direct Wallet Channel” served directly from the Highway network, enabling UI to be dynamically rendered. This new change in system architecture allows us to ***deploy frontend changes 25x quicker with 4x less code duplication***. 

4. Our end goal is a single input form that can take any kind of identifier, automatically associate with a Sonr Identity, and produces credentials via PassKeys. ***The ability to isolate authentication into this purest form is the pursuit of perfection we chase.***

![](assets/G2_cGiwXqLrOaG_-CWgkrfBA6oHTH7K_OU9xDN_ptIk=.blob)

###### 📌 **Importance on getting secure production ready codebase, and taking necessary compromises to accelerate our GTM.**

1. We’re*“full sending” *our cloud credits to get production ready infra. In order to maximize the compatibility of our wallet with the existing Web3 Market, we’ll be running our own Ethereum Testnet/Mainnet nodes using [GCP Blockchain Engine](https://cloud.google.com/blockchain-node-engine?hl=en). Therefore our Ethereum Wallet users will be able to directly communicate with the Ethereum network over a closed VPC of our resources. We plan to use this bandaid approach until a suitable IBC solution for Ethereum transaction finality has been addressed.

2. We’re essentially creating “Tokenized Identity-as-a-Service” - we have been allocating an increased amount of time towards our Airdrop Strategy, Bootstrap Liquidity Pools, and [Liquid Staking Module](https://medium.com/@DragonStake/introducing-liquid-staking-in-cosmos-the-gaia-v12-upgrade-and-its-implications-53e777c46b23) for Interchain assets. We anticipate Sonr to provide a unique value proposition to the larger Cosmos ecosystem and provide a rigid set of use cases for the Sonr token - along with revenue opportunities from cross-chain assets, outside purely authentication.

***

## Revamping the Sonr Codebase

I spent the majority of my engineering hours last year streamlining the codebase to be a [hypermedia system](https://hypermedia.systems/hypermedia-components/) and [monolith repository](https://github.com/sonrhq/sonr). Validator node operators now will have the inherent benefit of being able to serve a Gateway which can dynamically render frontend UI. 

![](assets/afWvwv0CD-O-jRNS8HUysKYUZgK648rQ3sUhXipKjuc=.blob)



##### Impact on Future Recruitment

In the past we looked for Blockchain savvy engineers with fundamentals in traditional Computer science with a knack for creating practical user experiences. With the aleviation of time, money, resources invested into frontend due to the new repo structure - we can now prioritize the recruitment of senior developers with robust experience in cybersecurity.

![](assets/wfs3psi7f4PpJF8yywwAK9jSSczyMH5NYX4yulO46QE=.blob)

The additional benefits of the repository refactor will show with time. This is because feature deployments, bug fixes, and general improvements can be quickly iterated and deployed without having to touch frontend specific code.

***

## “Sonr Mind”: AI Content Engine

Correctly leveraging the AI Tools which have already demonstrated “extra-human” ability in business operations has been a leading side initiative for the past year. This is being completely build out using No-Code tools hosted on Retool in order to minimize the development spikes that may arise with core development *(I used to be *[more involved in AI ](https://github.com/prnk28)*than crypto back in college 4 years ago. Sticking with no-code tools is a way to set a physical cap on my effort).*

![](assets/schHTgCKcx99d6JBM25USOG6PGdKoONx3D-dmP1HtZ0=.blob)

AI has great potential to assist in many areas of the business which when compared to product development have been lacking. Therefore, having a full fleet of GPT Agents to aleviate common business situations has been paramount for internal operations. This includes Issue Labeling, Pull Request Reviews, Project Migrations, Code Documentation, Milestone Planning, Content Generation by Audience, Relationship based Outreach, and Industry Signal Processing.

##### Next Marketing Campaign

Winning [Hackernoon's Startup of the Year](https://hackernoon.com/startups/north-america/north-america-brooklyn-nyc-ny), gets us a branded article on their website which would provide us with rich organic traffic to our target audience. We anticipate to use this aricle to introduce Sonr, announce the public testnet, and to provide users with early access codes to the Chat App.

![](assets/WCqE8BLvSDMKsWyWo_mBP1EqcDGiwxo3_3BXHobNeQ0=.blob)

Our plan is to capitlize on this growth in order to have a more public facing product hunt launch for the Mobile chat application. We feel that a bottoms-up approach of onboarding users and capitalizing on the developers to follow is a way to differentiate ourselves amongst the[ IBC Ecosystem](https://cosmos.network/ecosystem/tokens).

***

# Next Steps

We are currently working on completing the following initiatives:

1. Getting the Web App to production and available to beta users

2. Creating the Sonr and Osmosis Token Pool Smart Contract

3. Providing a ramp for Investors to register accounts prior to launch (allowlisting)

4. Producing a Network Launch Video

5. Creating a full screencast overview on Sonr, in order to add to our Deck

6. Re-Kickstart our Fundraising Round after building momentum

Feel free to get in touch with me on [Telegram](https://pradn.me/telegram), or Schedule a [quick call](https://cal.com/pradn/quick-chat) for any further questions!




**Best,**

**Prad Nukala**
