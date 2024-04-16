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
