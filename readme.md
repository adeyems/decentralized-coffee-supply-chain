# Decentralized Coffee Supply Chain
## A decentralized app that track coffee supply from a farmer to the final consumer. It runs on Ethereum blockchain.

### Roles
- **Farmer**: Harvests, Processes, Packs and Sells coffee to the **Distributor**.
- **Distributor**: Buys coffee from the **Farmer** and Ships the coffee to the **Retailer**.
- **Retailer**: Receives coffee from the **Distributor**.
- **Consumer**: Purchase coffee form the **Retailer**

## Project Write-Up

### UML Diagrams

[State Diagram](./uml-diagrams/state-diagram.png)<br>
[Activity Diagram](./uml-diagrams/activity-diagram.png)<br>
[Sequence Diagram](./uml-diagrams/sequence-diagram.png)<br>
[Data Model](./uml-diagrams/class-diagram.png)<br>

### Libraries

[**Truffle**](http://truffleframework.com/): Used in development, testing and deploying the smart contracts.

## Contract Details

Transaction Hash: [0xb960fbb8d12132db5f288c0d3bb444ae4982c944947b473d2cb3c50cbc8fc222](https://rinkeby.etherscan.io/tx/0xb960fbb8d12132db5f288c0d3bb444ae4982c944947b473d2cb3c50cbc8fc222)<br>
Contract address: [0x7d90f7541427d3f0b1e03044b3d03b291bc1ce77](https://rinkeby.etherscan.io/address/0x7d90f7541427d3f0b1e03044b3d03b291bc1ce77)<br>

## Development Notes
**Node v16.15.0**<br>
**Truffle v4.1.14 (core: 4.1.14)**<br>
**Solidity v0.4.24 (solc-js)**<br>
**Ganache CLI v6.12.2 (ganache-core: 2.13.2)**<br>
**Web3 v1.2.4**


## Installation
- Clone the repo
- Run ``npm install``
- Run ``npm run compile`` to compile the contract
  ``` 
    Compiling ./contracts/Migrations.sol...
    Compiling ./contracts/coffeeaccesscontrol/ConsumerRole.sol...
    Compiling ./contracts/coffeeaccesscontrol/DistributorRole.sol...
    Compiling ./contracts/coffeeaccesscontrol/FarmerRole.sol...
    Compiling ./contracts/coffeeaccesscontrol/RetailerRole.sol...
    Compiling ./contracts/coffeeaccesscontrol/Roles.sol...
    Compiling ./contracts/coffeebase/SupplyChain.sol...
    Compiling ./contracts/coffeecore/Ownable.sol...
    Writing artifacts to ./build/contracts

  ```
- Run ``npm test`` to run the tests. 
    ```
    Using network 'development'.

    ganache-cli accounts used here...
    Contract Owner: accounts[0]  0x27d8d15cbc94527cadf5ec14b69519ae23288b95
    Farmer: accounts[1]  0x018c2dabef4904ecbd7118350a0c54dbeae3549a
    Distributor: accounts[2]  0xce5144391b4ab80668965f2cc4f2cc102380ef0a
    Retailer: accounts[3]  0x460c31107dd048e34971e57da2f99f659add4f02
    Consumer: accounts[4]  0xd37b7b8c62be2fdde8daa9816483aebdbd356088

      Contract: SupplyChain
        ✓ Testing smart contract function addRole() for assigning various user roles  (207ms)
        ✓ Testing smart contract function harvestItem() that allows a farmer to harvest coffee (99ms)
        ✓ Testing smart contract function processItem() that allows a farmer to process coffee (62ms)
        ✓ Testing smart contract function packItem() that allows a farmer to pack coffee (65ms)
        ✓ Testing smart contract function sellItem() that allows a farmer to sell coffee (61ms)
        ✓ Testing smart contract function buyItem() that allows a distributor to buy coffee (219ms)
        ✓ Testing smart contract function shipItem() that allows a distributor to ship coffee (58ms)
        ✓ Testing smart contract function receiveItem() that allows a retailer to mark coffee received (78ms)
        ✓ Testing smart contract function purchaseItem() that allows a consumer to purchase coffee (68ms)
        ✓ Testing smart contract function fetchItemBufferOne() that allows anyone to fetch item details from blockchain
        ✓ Testing smart contract function fetchItemBufferTwo() that allows anyone to fetch item details from blockchain
    ```
- Create metamask.secret and infura.txt file and put your metamask secret and infura key into the respective files
- Run ``npm run deploy`` to deploy to rinkeby network
- 
- Run ``npm run dev`` to serve the project locally and interact with the frontend at [localhost:3000](http://localhost:3000)

