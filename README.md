# What it does
The DAO Tokenized Voting Power Allocation System is a tool that allows DAO users to implement flexible voting power systems based on crypto token deposits. This system integrates with Redmine, a popular project management tool, enabling decentralized governance mechanisms where users can vote on project features, issue resolutions, or development priorities by staking tokens. The plugin helps DAOs align their interests with the wider community while incentivizing contributions to software development.



# The problem it solves
One of the main challenges in open-source development and DAO governance is the disconnect between users who want specific features and the developers responsible for implementing them. Often, individual entities lack the resources or incentives to push forward development on desired features or bug fixes. The Tokenized Voting Power System addresses this by distributing the cost of development and bug fixes among multiple parties through token-based voting. This allows for decentralized decision-making, ensuring that the most demanded features are prioritized while aligning incentives for both users and developers.



# Challenges I ran into
Token Integration: Ensuring seamless integration of crypto tokens (such as Bitcoin and testnet versions) within the Redmine ecosystem was challenging, especially dealing with compatibility across various versions of Redmine, Ruby, and Rails.

RPC Server Configuration: Setting up and managing the bitcoind RPC servers for different tokens required detailed configuration and troubleshooting.

Security Concerns: Ensuring the plugin did not inadvertently encourage the use of insecure hot wallets for token voting required careful design, with specific limitations on handling private keys.

User Onboarding: Simplifying the complex setup process for end users, including managing Redmine permissions, enabling REST services, and configuring RPC daemons.



# Technologies I used
edmine: Project management tool used as the base for this plugin.

Ruby on Rails: The framework behind Redmine, used for building and managing the plugin.

Bitcoind RPC (Bitcoin Core): Used for integrating token deposits as part of the voting mechanism.

Token Voting Plugin: Custom plugin built to enable token-based voting in Redmine.

BTCTEST: Testnet version of Bitcoin used for testing token deposits and votes.



# How we built it
We started by integrating the Token Voting Plugin into a standard Redmine environment. The backend was set up using Ruby on Rails and the plugin was designed to interact with bitcoind RPC to allow users to vote using Bitcoin or testnet tokens. Configuration settings were added to allow for REST API integration, role-based permission management, and token voting mechanics. Finally, we ensured the system was flexible enough to work with different token types and versions by setting up checkpoint mechanisms to track the progress of votes and issue resolutions.