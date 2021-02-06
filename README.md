## Grasshopper - Digital Signature Exchange Interface 
### ETHDenver 2021  - ColoradoJam - Public Infrastructure 
Grasshopper is a minimalist interface to mint & exchange digital signatures or attestations.  

Signatures & metadata can be (in theory) linked to self sovereign identities, pinned to IPFS (maybe Ceramic?), broadcast to Web3, or pushed to an API. 

For the ColoradoJam proof of concept we aim to show how Grasshopper can be used to license a new business, state parks pass, hunting or fishing license, or to mint a digitally signed gaming license that powers not-for-profit game of chance on Ethereum.  
 
## How does Grasshopper work? 
[insert-diagram](diagram-here)

A Grasshopper signature exchange consists of three main steps. Each step can be done in person, or over a network. 

We will show how an in person signature exchange can be done to strengthen certain security properties of the exchange by reducing sybil attack vectors. Future versions could incorporate [Minimal Anti-Collusion Infrastructure](https://github.com/appliedzkp/maci) to further expand into use cases where collusion could be a problem.   

In this example, the License Minter would be the state of Colorado and the License Applicant would be the individual applying for the license.  

1) Initiate Application - The License Minter displays an address to the License Applicant to initiate the application - **The applicant initiates the application process by sending an transaction to License Minter address**. This step can optionally require the license applicant to submit a fee with the transaction. 

2) Collect Metadata, verify ID, sign & broadcast message - License Minter collects metadata, optionally encrypts and stores metadata**, signs a message, and then **License Minter broadcasts digital signature to a license registry contract.**

3) Confirm Application, sign & broadcast message, receive Digital License NFT - Finally, the License Applicant signs a message from their address and broadcasts this to the License registry contract to complete the application process. **A Digital License NFT is then sent to Applicants address.** 

## Design Discussion 
The three step process above could probably be reduced down to two steps in some cases. At the same time, using a three step process does also give some extra flexibility. For example, step one could be done over the internet ahead of time, and then steps two and three could be done in person in cases where human verification of ID is important. 

## Disclaimer
Grasshopper is experimental software. Design challenges around privacy and security are immense and we have not yet addresses all these challenges :) 

**Not yet implemented - 

