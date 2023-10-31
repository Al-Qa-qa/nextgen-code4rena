# Refactored and More Professional NextGen Code4rena Smart Contract Development Code.

The NextGen is now alive on code4rena (30 Oct 2023 to 13 Nov 2023), but the code structure is not so good to deal with and start auditing.

## Problems in this code structure
- All smart contracts in one folder.
- OpenZeppelin contracts are imported locally in the same Smart contract directory.
- No linting processes occur.
- Lack of tests, even some smart contracts have 0 coverage results.

## How to install this new version
1. Start by cloning the project into your folder:
  ```
  git clone https://github.com/Al-Qa-qa/nextgen-code4rena
  ```
2. Go the project directory:
  ```
  cd /nextgen-code4rena
  ```
3. Install packages:
  ```
  npm install
  ```

## Available Scripts to use
- `npm run compile`: Compile (.sol) files
- `npm run test`: Run tests 
- `npm run coverage`: Run coverage
- `npm run local-blockchain`: Make local blockchain similar to anvil in case of Foundry
- `npm run lint`: Lint solidity file (simple static analysis)
- `npm run slither`: Run slither static analysis

## New Features
- in `/contracts` we grouped unnecessary contracts in separate folders. For example, we made a folder called `openzeppelin` and put OpenZeppelin contracts in it.
- Made a separate file for the Interfaces
- Put the .sol files that are out of the scope in the `out-scope` folder.
- Files in the scope are (.sol) files that come directly after the `/contracts` folder (/contracts.*sol)
- Changing the name of the contracts to match the file name, to avoid conflicts.
- Instead of previous gas results on the terminal, the gas will be previewed in a separate file `gas-report`, so if you want to make gas checks go on.

Hope this helps you wardens in auditing NextGen.

Follow us on Twitter for more interesting information about smart contract auditing, [@Al-Qa-qa](https://twitter.com/Al_Qa_qa)

