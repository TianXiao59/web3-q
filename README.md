# web3-q

`npm install --save-dev web3-q`

Web3-Q is not meant for production, but for unit testing purposes (see chaithereum). Ironically, it does not contain unit tests beyond what exists in the Web3 repo.

Version numbers are set to match those of the canonical web3 repo. If this repo falls behind that web3, please leave an issue and I will manually update.

Thanks!

-Aakil

## Additional Functions

    web3.eth.method.q(...).then(...)
    ContractFactory.new.q(...).then(...)
    contract.method.q(...).then(...)
    contract.method.estimateGas.q(...).then(...)
    contract.filter(...).q(...).then(...)

### Examples

    web3.eth.getBalance.q('0x...').then((balance) => {...})
    MyContractFactory.new.q({ data: ... }).then((MyContract) => {...})
    MyContract.owner.q().then((_owner) => {...})
    MyContract.setOwner.estimateGas.q('0x...').then((gas) => {...})
    MyContract.OwnerChanges(...).q(...).then((results) => {...})