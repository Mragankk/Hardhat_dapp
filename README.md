# HARDHAT dAPP
Pre-requisites -
```npm``` and  ```Node JS (version >=18.0)```

## Installing Hardhat using npm inside a dir
- initialize an npm project
```
npm init
```
- Now install Hardhat
```
npm install --save-dev hardhat
```
- In the same directory where you installed Hardhat run:
```
npx hardhat init
```
- Now Select ```Create a hardhat.config.js```

When Hardhat is run, it searches for the closest hardhat.config.js file starting from the current working directory. This file normally lives in the root of your project and an empty hardhat.config.js is enough for Hardhat to work. The entirety of your setup is contained in this file.

![image](https://github.com/Mragankk/Hardhat_dapp/assets/145200189/30244ad5-401c-411f-b11e-f1606b562eb5)

- Install the Hardhat plugin for ethers.js, we will use recommended plugins 
 ```
     npm install --save-dev @nomicfoundation/hardhat-toolbox
 ```
- Add the following lines to hardhat.config.js
```
require("@nomicfoundation/hardhat-toolbox");
```
![image](https://github.com/Mragankk/Hardhat_dapp/assets/145200189/4a3a6ffb-78eb-4aed-8361-c8d7308812af)

## Writing and Compiling Contracts
- Make a ```Token.sol``` (or file with any name) and wirte a basic contact in it
- To compile the contract run ```npx hardhat compile``` in your terminal.
  
  ![image](https://github.com/Mragankk/Hardhat_dapp/assets/145200189/f7fce044-5394-4198-aad1-d54134f335d5)

## Testing Contract
- Writing automated tests when building smart contracts is of crucial importance, as your user's money is what's at stake.

- To test our contract, we are going to use Hardhat Network, a local Ethereum network designed for development. It comes built-in with Hardhat, and it's used as the default network. You don't need to setup anything to use it.

- In our tests we're going to use ethers.js to interact with the Ethereum contract we built in the previous section, and we'll use Mocha as our test runner.

- Creating a new directory 'test' inside the project root directory and creating a new file in there called 'Token.js'.
- run the command in terminal
  ```
  npx hardhat test
  ```

   ![image](https://github.com/Mragankk/Hardhat_dapp/assets/145200189/8afc1639-be5b-4145-9bb2-5a3f2f877eb6)
## Deploying to a live network (hardhat)
- In Hardhat Ignition, deployments are defined through Ignition Modules. These modules are expected to be within the ./ignition/modules directory.
- If aleady not made , make new directory ```ignition``` inside the project root's directory, then, create a directory named ```modules``` inside of the ignition directory.
- Make ```Token.js``` inside same directory and paste below code in it:
```
const { buildModule } = require("@nomicfoundation/hardhat-ignition/modules");

const TokenModule = buildModule("TokenModule", (m) => {
  const token = m.contract("Token");

  return { token };
});

module.exports = TokenModule;
```
- To tell Hardhat to connect to a specific network, you can use the --network parameter when running any task, like this:
```
npx hardhat ignition deploy ./ignition/modules/Token.js --network <network-name>
```


  ![image](https://github.com/Mragankk/Hardhat_dapp/assets/145200189/ad99f33e-8d77-4540-945a-9c1d643129f5)
