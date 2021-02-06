## Grasshopper - Digital Signature Exchange Interface Setup 

For the ETHDenver 2021 POC we're just going to serve up the Grasshopper interface with a locally hosted http server and either a local Ganache Ethereum blockchain or maybe Rinkeby if we have time. 


### 1) Setup for local testing

#### 1A) Hosting local HTTP server
First, lets make sure we have a local http server setup to serve the Grasshopper signature exchange application. For non-production/POC purposes we can run a local http server with python or node. You can use either of the following:

With Python [http.server](https://docs.python.org/3/library/http.server.html):

`python3 -m http.server 42000`

Or [http-server](https://www.npmjs.com/package/http-server) with Node: 

`http-server -p 42000`


#### 1B) Running a local Eth node 
If you're using a development framework like Brownie you can just let it handle running the local blockchain for you. 

If you want to test with a local ETH node you can use [Ganache-cli](https://github.com/trufflesuite/ganache-cli) like this:

```bash
npx ganache-cli \
  -f https://mainnet.infura.io/v3/<your-infura-key-here> \
  -m "clutch captain shoe salt awake harvest setup primary inmate ugly among become" \
  -i 1337 
```

### 2) Setup for Rinkeby testing
TODO


### 3) setup for Mainnet 
TODO

