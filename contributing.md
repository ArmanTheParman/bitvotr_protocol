# Contributing

Thank you for contributing to this project. 
This page will be frequently updated, and serves as a starting point for things that I need to do, and things that I could use help with.

### Review Whitepaper
Suggestions to improve readability are welcome via pull requests.
The latest change after several people have already reviewed, is the introduction of "proof-of-tax".
I will split the Appendix into a Q&A and a proper appendix.
The good questions I'm responding to in private comments will be added (including any asked in the GitHub issues sections).

### Networking
Currently, the protocol specifies using Tor for peer-to-peer communication. This will only work for small elections. If scaling to 300M
people, as I understand it, the Tor network will not be able to tolerate the required bandwidth, and nor will it tolerate the creation
of 300M hidden services.

When considering an alternative, it's important to recognise the need to hide IP addresses, as they are associated with identities. When a
public key and and IP come together, too much information is revealed about a voter, and their vote can be exposed, or at least, there will
be the concern by voters that it could be exposed.

As a potential candidate, I am considering HolePunch, a system used by Keet. I need advice about how and if IPs will be hidden.

Another is Veiled, which as I understand won't have the IP address problem, but I am unsure if it can scale.

### RAFT
The Raft protocol is well described and a decision needs to be made about whether to create libraries from scratch or use existing libraries
and from which programming language. This might influence which language to use for the BitVotr app overall.

Thought needs to be given to the process of selecting the very first leaders to defend against an orchestrated leader attack. I'm thinking to double hash the starting Bitcoin block to use the randomness to determine which of the seven nodes in the initial clusters becomes leader. 

