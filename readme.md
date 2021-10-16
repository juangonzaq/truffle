# First's step H1 
1. Install ganache
2. Install truffle: npm install truffle -g
3. Change setting: truffle-config.js using credentials ganache
4. Compile truffle: truffle deploy --network development

# Important: H6
If you restart your computer or closed ganache, you must first run: truffle reset

# Truffle console #H2
truffle console --network development
1. Show accounts in ganache in console truffle : web3.eth.getAccounts(function(err, acc) { accounts = acc});
2. Get balance first account: web3.eth.getBalance(accounts[0]);
3. Convert from wei to ether:  const convertToEther = async () => { return web3.utils.fromWei(await web3.eth.getBalance(accounts[0]), 'ether'); } 

or: const etherValues = web3.utils.fromWei('1000000000000000000', 'ether');
inverse: const weiValue = web3.utils.toWei('1', 'ether');

4. Send transaction: web3.eth.sendTransaction({ from: accounts[0], to: accounts[1], value: web3.utils.toWei('15', 'ether')});
5. Get transaction detail: web3.eth.getTransaction('0x55f7e5ab74255a619576454fb1fdf0a97028b606667249facc390067e98ff857');