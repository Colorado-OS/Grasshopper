## Grasshopper - Digital Signature Exchange Interface 
### ETHDenver 2021  - ColoradoJam - Public Infrastructure 
Grasshopper is a minimalist interface to mint & exchange digital signatures or attestations.  

Signatures & metadata can be (in theory) linked to self sovereign identities, pinned to IPFS (maybe Ceramic?), broadcast to Web3, or pushed to an API. 

For the ColoradoJam proof of concept we aim to show how Grasshopper can be used to license a new business, state parks pass, or to mint a digitally signed gaming license that powers not-for-profit game of chance on Ethereum.  
 
## How does Grasshopper work? 
[insert-diagram](diagram-here)

A Grasshopper signature exchange consists of two main steps. Each step can be done in person, or over a network. 

We will show how an in person signature exchange can be done to strengthen certain security properties of the exchange by reducing sybil & collusion attack vectors.  

In this case, the License Minter (LM) would be the state of Colorado and the License Applicant (LA) would be the individual applying for the license.  

1) The License Minter (LM) provides an address to the License Applicant (LA) - This could be from a QR code **The applicant initiates the application process by sending an transaction to LM address**. 

2) LM collects [m]etadata, optionally encrypts and stores metadata**, signs a message, and **License Minter broadcasts digital signature to a Web3 license registry contract.** A digitally Signed Gaming License NFT is sent to Applicant's address. 

## Disclaimer
Grasshopper is experimental software. Design challenges around privacy and security are immense and we have not yet addresses all these challenges :) 


**Not yet implemented 


