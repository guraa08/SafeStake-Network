# SafeStake-Network
You need 32 Ropsten Eth 
Faucet https://faucet.egorfine.com/ 

1. Open https://testnet.safestake.xyz/
2. Run Validator > direct to https://ropsten.launchpad.ethereum.org/en
3. Click I accept 
4. Choose Geth > continue
5. Choose Lighthouse > continue
6. Generate Key Pairs validator 1 > Choose linux > build form source
7. open your vps/termux/powershell ( you dont need vps ,just need terminal )
8. sudo apt update && apt install python3-venv python3-pip python3-virtualenv
9. git clone -b master --single-branch https://github.com/ethereum/staking-deposit-cli.git
10. virtualenv venv
11. source venv/bin/activate
12. cd staking-deposit-cli
13. python3 setup.py install
14. pip3 install -r requirements.txt
15. python3 ./staking_deposit/deposit.py new-mnemonic --num_validators 1 --chain ropsten
16. Save your mnemonic. If you use vps, download keystore and deposit data on /root/staking-deposit-cli/validator-keys
17. Back to ropsten site, upload your deposit data json > continue > connect wallet > continue > confirm deposit > continue
18. Your validator is ready to run now
19. Go to https://testnet.safestake.xyz/
20. Import your keystore ,type your password when creating validator key
21. Choose 4 operator ( its up to you ) > next > Run Validator
22. Your validator is now running, you can shutdown your vps
