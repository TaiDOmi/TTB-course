# h4 To The Moon!

## x) Read and summarize (with some bullet points)
_Nakamoto 2008: Bitcoin: A Peer-to-Peer Electronic Cash System (A colored HTML version), chapters_

Source: _https://git.dhimmel.com/bitcoin-whitepaper/_

**1 Introduction**
- Commerce on the Internet suffers from the weaknesses of trust based model (Financial institutionshandling the payments)
  - Not possible to make non-reversible transactions
  - Limits the possiblity to make small transactions because of costs
- Electronic payment system based on cryptographic proof is needed
- Seller protection from fraud because transactions are almost impossible to reverse
- System is secure as long as there are more honest nodes than mlicious nodes in control

**2 Transactions**
- Electronic coin is a chain of digital signatures
  - Previous owners are saved to the hash of a new transaction by adding a public key of the next owner to the end of the coin hash.
- Need a way to be sure that there are no double payments
  - Earliest transaction counts
  - Transactions need to be public and majority of the nodes need to agree that the transaction was the first received 

**3 Timestamp Server**
- A timestamp server needed.
  - A chain of timestamps where every new timestamp confirms the previous timestamps in the hash

**4 Proof-of-Work**
- Proof-of-work system scans a value when hashed (SHA-256)
- The hash begins with a number of zero bits
- A nonce is incremented in the block until a value with required zero bits is found.
- A block cannot be changed after the proof-of-work without redoing the work (all the blocks after the block that was changed).
- The difficulty of proof-of-work is defined by an average moving target of block per hour. The difficulty to create proof-of-work increases if blocks are generated too fast.

**5 Network**
- Network nodes always consider the longest chain to be the correct one.
- If two versions of the next block is done simultaneously the nodes work with the one that they first received but also save the other branch in case it becomes longer and change to work on it if it happens.
- If a block is not received, a node will request it 

**6 Incentive**
- The first transaction starts a new coin and is owned by its creator.
  - Works as an incentive to publish more coins and support the network.
- The incentive can move to transaction fees completely after a prenumbered coin amount are in circulation.
- More profitable to mine new coins than trying to fraud the system or people.

## a) Wallet. 
_Create a BitCoin testnet wallet._

Source: _https://terokarvinen.com/trust-to-blockchain/#homework_

- Update apt-get
  - $ sudo apt-get update
- Install a coin wallet (Electrum)
  - $ sudo apt-get install electrum; electrum --testnet # from memory
  - Name of the wallet "Tomitest_wallet"
  - Created a standard wallet without a multi-factor authentication
  - Selected "Create a new seed"
  - Seed for the test wallet (no real money so no risk of putting it here):
![image](https://github.com/user-attachments/assets/9940ab05-609d-408e-85c1-a15c98b1c15b)
  - Wallet created
![image](https://github.com/user-attachments/assets/27abb895-3e70-4126-bbcf-7a3f22a3bf08)

## b) Faucet. 
_Get worthless fake money from a testnet Bitcoin faucet._

Sources: _https://bitcoinfaucet.uo1.net_, _https://coinfaucet.eu/en/btc-testnet/_

- Copied the wallet address
![image](https://github.com/user-attachments/assets/5437afcf-0493-4e44-95dd-194d842c8cb1)
- Got money from coinfaucet (https://coinfaucet.eu/en/btc-testnet): 
![image](https://github.com/user-attachments/assets/489357f7-5491-4c0a-92e3-5c111bc9b815)
- Money in the wallet:
![image](https://github.com/user-attachments/assets/9aadeda1-2075-46b5-a3c1-10571b928220)
- Changed unit from mBTC to BTC
![image](https://github.com/user-attachments/assets/431b753c-2880-46cc-bfb2-de13e058c1e0)

## c) Giveway. 
_Move money to another Bitcoin wallet. Choose an amount where the last two digits are 73._

- Establish another wallet from File/New "Tomitest_wallet_2"
![image](https://github.com/user-attachments/assets/b2a84ed7-1763-4ab3-8376-b06dc4b43cd4)
- Move money from Tomitest_wallet to Tomitest_wallet_2
![image](https://github.com/user-attachments/assets/1005d422-cbe6-450d-991b-614c5d539b0d)
- Not enough funds
![image](https://github.com/user-attachments/assets/31519589-8fac-47c0-86f8-0c94e98f6c50)
- Changed to mempool and tried again - mempool min fee not met
![image](https://github.com/user-attachments/assets/a2e0f37a-aa8b-43cb-bb9c-b286535a2617)
- 2nd try with bigger sums
![image](https://github.com/user-attachments/assets/f859e97c-c7bb-4cc4-9e97-a041ae58bfda)
- Changed Fee rate to Static: min
![image](https://github.com/user-attachments/assets/3f1deda8-466f-421e-8628-3513cebb6baa)
- 
- Tried to get more money from _cryptopump.info/_
![image](https://github.com/user-attachments/assets/b5daaf08-bb50-40a5-a114-34ad2c5172f7)
![image](https://github.com/user-attachments/assets/19ffffb8-45e8-41d4-9a53-4c699bb06b39)
- It seems to be hard to get even test Bitcoins.
- I have to wait 11 hours to get more money from coinfaucet.
- 

## d) Recycle. 
_Move the testnet money back to the same faucet you got it from._

Cannot do because I could not send money to the second wallet.

## e) Explorer. 
_Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. 
You only need to analyze the block information and one sample transaction, as a block can contain many transactions. 
Voluntary bonus: Use a transaction that's interesting, such as one related to a crime or other unusual event._

Sources: _https://blockexplorer.one/, https://www.coinbase.com/learn/crypto-basics/bitcoin-block-reward-block-size-block-time-whats-the-difference_

- Selected the latest block transaction on the bBlock Explorer for analyzation.
![image](https://github.com/user-attachments/assets/17231466-6118-4f37-b4cc-0de09492f1cd)

- Block size (1674430 bytes):
  - The amount of data that can be stored in a block. A block is a set of bicoin transactions for a time-period. The zize is normally around 2 MBs (up to 4 MBs) so this a a smaller block than average.
- Difficulty (101.65 TH):
- Received Time: Time when the transaction was received by the payee.
- Rewards (3,125 BTC)
  - A reward for miners for validating blocks of transaction (Miners contribute computing power to maintain the Bitcoin blockchain)- The reward halves about every four years (or every 210,000 blocks). 
- Total Transactions (3,357) :
  - There are 3357 transacions in the block (average 3990 on 18.11.2024). 
- Block Hash (000000000000000000005ecb9df0be545ad85e74fd42545e110f8527a7a3fd43):
  - The unique reference for a block in a blockchain. 
- Confirmations (1)


## f) RogeCoin. 
_Critically comment on Honest Ads: If Cryptocurrency Was Honest (Video, about 5 minutes). 
Identify and list arguments made. Provide commentary to support and challenge each of the claims. 
If you can, provide references or real life examples to your claims. (This task does not require tests with a computer.)_

Source: _https://www.youtube.com/watch?v=GUs5y9leCyA_

- Computer cash is easy to lose, volatile and not good for the environment
- Cannot be exchanged for most of goods and services
- Roge coin is created by computers solving needlessly complicated math problems using more power than Switzerland.
- Real money will become worthless when government collapses but Roge coin will remain its value as long as there is a talk about it in the Internet.
- Your money is yours forever unless you give them to a scammer, or get hacked, or the hard-drive where your walllet is fails, or forget your password.
-  Common purchase drugs and sex
-  very volatile: Can triple its value overnight or lose all its value if someone with an influence tweets about it, or a country bans it.
-  It's money that should be hoarded forever
-  A cult
-  Most of the Roge coin has already been mined and need a lot of CPU power to mine
-  





3
