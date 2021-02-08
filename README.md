## Grasshopper - Digital Signature Exchange Interface 
### ETHDenver 2021  - ColoradoJam
Grasshopper is a minimalist interface to mint & exchange digital signatures,  attestations, or Web3 transactions.  

Signatures & metadata can be linked to self sovereign identities, pinned to IPFS with [Ceramic & IDX](https://blog.ceramic.network/building-with-decentralized-identity-on-idx-and-ceramic/), broadcast directly to Web3, and/or just pushed to an API.

💡 Grasshopper has been bootstrapped from these awesome [Compound.Finance governance examples](https://github.com/compound-developers/compound-governance-examples) that use EIP712 signed messages for voting and delegation.💡 

For the ColoradoJam proof of concept we aim to showcase how [Colorado OS](https://github.com/Colorado-OS/eth-contracts) & Grasshopper can be used to issue a defi charged digital state parks pass and also to mint a digital players gaming license (NFT) that powers not-for-profit game of chance on Ethereum.  

The current design leverages a bare minimum local webserver to host signature exchange components & is designed to run on an air-gapped raspberry pi or something similar. 

Moving forward we envision Grasshopper exchange interfaces also existing as a series of minimal verifiable UIs on the decentralized web similar gold standard of [app.uniswap.org](https://uniswap.org/blog/ipfs-uniswap-interface/)      
___
## How does Grasshopper work? 
[create-pretty-diagram](diagram-here)

For our ETHDenver use cases a Grasshopper signature exchange consists of three main steps. Each step can be done in person, or over a network. 

We will [show how an in person signature exchange](https://docs.google.com/document/d/1682GssIrPVFe08DNPi27LB7IkAwc_gUz1Rpt8Y2dJkQ/edit) can be done to strengthen certain security properties by reducing sybil attack vectors. Future versions could incorporate [Minimal Anti-Collusion Infrastructure](https://github.com/appliedzkp/maci) to expand into use cases where collusion resistance is needed (users asserting preference ;).  

In an generic example, the License Minter would be the state of Colorado and the License Applicant would be the individual applying for the license, pass, or other state token.  

1) **Initiate Application** - The License Minter displays an address to the License Applicant to initiate the application - **The applicant initiates the application process by sending an transaction to License Minter address**. This step can optionally require the license applicant to submit a fee with the transaction. 

2) **Collect Metadata, Verify ID, Sign & Broadcast Message** - License Minter collects metadata, optionally encrypts and stores metadata with [Ceramic & IDX](https://blog.ceramic.network/building-with-decentralized-identity-on-idx-and-ceramic/), signs a message, and then the **License Minter broadcasts digital signature to a license registry contract.**

3) **Confirm Application - Sign & Broadcast Message, Mint Digital License NFT** - Finally, the License Applicant signs a message from their address and broadcasts this to the License registry contract to complete the application process. **A Digital License NFT is minted & issued to passport holder, player, or other recipient via self sovereign DID pointer/record.** 

---
## What else could Grasshopper be used for?
Having a signature exchange board might be useful for Web3. Verifiable snippets of distributed Web2 code running in Web3 sounds nice too.  
___
## Design Discussion 
Human verification of ID is an important feature of Grasshopper & Colorado OS. As we understand it, this could help to optimise the [MACI framework](https://github.com/appliedzkp/maci) and reduce the efficacy of collusion attacks to a reasonable place. This is an exciting prospect.   
___
## Disclaimer
Grasshopper is experimental software. Design challenges around privacy and security are immense. Grasshopper and related Colorado OS contracts need to be reviewed and audited. 

---

 ❤️🧡💛💚💙💜 ETHDenver 2021 - ColoradoJam  ❤️🧡💛💚💙💜



