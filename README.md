# TA Write Up

## Project Brief

Fair Trade Coffee is a blockchain Proof-of-Concept for tracking how your coffee beans arrive from Farmer to Consumer

## Supply chain & data auditing

This repository contains an Ethereum DApp that demonstrates a Supply Chain flow between a Seller and Buyer. The user story is similar to any commonly used supply chain process. A Seller can add items to the inventory system stored in the blockchain. A Buyer can purchase such items from the inventory system. Additionally a Seller can mark an item as Shipped, and similarly a Buyer can mark an item as Received.

# Project Specification

## Write Up

### Project write-up include the following UML diagrams:

 - Activity
 <p float="left">
    <img src="https://raw.githubusercontent.com/endikaaguilera/myreposassets/master/supply_chain/ActivityDiagram.jpg" width="600" />
</p>
 
 - Sequence
<p float="left">
    <img src="https://raw.githubusercontent.com/endikaaguilera/myreposassets/master/supply_chain/SequenceDiagram.jpg" width="600" />
</p>
 
 - State
 <p float="left">
    <img src="https://raw.githubusercontent.com/endikaaguilera/myreposassets/master/supply_chain/StateDiagram.jpg" width="600" />
</p>
 
 - Classes (Data Model)
<p float="left">
    <img src="https://raw.githubusercontent.com/endikaaguilera/myreposassets/master/supply_chain/DataDiagram.jpg" width="600" />
</p>

### If libraries are used, the project write-up discusses why these libraries were adopted.

 - Truffle v5.5.12 (core: 5.5.12)
 - Ganache v^7.1.0
 - Solidity - 0.8.4 (solc-js)
 - Node v17.6.0
 - Web3.js v1.5.3
 
### If IPFS is used, the project write-up discusses how IPFS is used in this project.

 - IPFS: N/A - Not used in this project

## Write smart contracts with functions

 - Smart contract implements functions to track.
    - Product ID
    - Product UPC
    - Origination Information
    - Farm
    - Misc organization info
    - Longitude & Latitude of geo coordinates
    - Product notes
 
 - Ownable.sol has required functions that establish owner and the transfer of ownership.

 - ConsumerRole.sol has required functions that manage the consumer role.
  
 - RetailerRole.sol has required functions that manage the consumer role.

 - DistributorRole.sol has required functions that manage the consumer role.
 
 - Student has implemented additional roles correctly.

## Test smart contract code coverage

 - Project contains tests for the boiler plate functions and all tests are approved without error.

<p float="left">
    <img src="https://raw.githubusercontent.com/endikaaguilera/myreposassets/master/supply_chain/testing_results.png" width="600" />
</p>

 - Steps for testing:
    - $ truffle compile
    - $ truffle develop
    - open new terminal window/tab
    - $ truffle migrate --reset (optional)
    - $ truffle test

## Deploy smart contract on a public test network (Rinkeby)

### Contract Address:

EtherScan Contract Address: 0xdec659076be6c6a96e0acf0f1cee2963be2ce5be

[Contract Address](https://rinkeby.etherscan.io/address/0xdec659076be6c6a96e0acf0f1cee2963be2ce5be)

### Transactions History

 - Packed - 0xc34a2086731b05386acd598d3264c523f7c68e22b18a344e036951e78906b045
 - ForSale - 0x361ce725717e101d0bc404dc3e3c23fa016c5923f6f49664b9b223f5ebc4e0f6
 - Sold - 0xbc1c061a3ff04ea8282078c946f780ebbde4bfc3aa5e7795817940ba4f123574
 - Shipped - 0xe21df006fd063aa5d7d88c38fd59a594083113fd10eb120fd485356ff3b41b0f
 - Received - 0xaeb5df1e8c120e649fddee0912e114135bd4b58be7867c4092fb7c807c1ce68d
 - Purchased - 0xa2080b67804ddbcc7da8eb691580f2244bb98975366bc1238890690fb9148cb8

### Modify client code to interact with a smart contract

Front-end is configured to:
 - Submit a product for shipment (farmer to the distributor, distributor to retailer, etc).
 - Receive product from shipment.
 - Validate the authenticity of the product.

## Built With

[Ethereum](https://www.ethereum.org/) - Ethereum is a decentralized platform that runs smart contracts

[Truffle Framework](http://truffleframework.com/) - Truffle is the most popular development framework for Ethereum with a mission to make your life a whole lot easier.

## Acknowledgments

- Solidity
- Ganache-cli
- Truffle
