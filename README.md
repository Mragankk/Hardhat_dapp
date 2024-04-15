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
![Screenshot 2024-04-15 152032](https://github.com/Mragankk/Hardhat_dapp/assets/145200189/cbe2bb18-3b6f-4b9b-8f71-3e1513c221fe)

## Writing and Compiling Contracts
- Make a ```Token.sol``` (or file with any name) and wirte a basic contact in it
- To compile the contract run ```npx hardhat compile``` in your terminal.
