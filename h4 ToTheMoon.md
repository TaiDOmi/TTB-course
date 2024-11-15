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

- $ sudo apt-get 

## b) Faucet. 
_Get worthless fake money from a testnet Bitcoin faucet._

## c) Giveway. 
_Move money to another Bitcoin wallet. Choose an amount where the last two digists are 73._

## d) Recycle. 
_Move the testnet money back to the same faucet you got it from._

## e) Explorer. 
_Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. 
You only need to analyze the block information and one sample transaction, as a block can contain many transactions. 
Voluntary bonus: Use a transaction that's interesting, such as one related to a crime or other unusual event._

## f) RogeCoin. 
_Critically comment on Honest Ads: If Cryptocurrency Was Honest (Video, about 5 minutes). 
Identify and list arguments made. Provide commentary to support and challenge each of the claims. 
If you can, provide references or real life examples to your claims. (This task does not require tests with a computer.)_




