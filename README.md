# BlockShield: Securing Transactions Against Double Spending

BlockShield is an educational blockchain simulation built in Node.js to detect and mitigate double-spending attacks.
It combines Proof-of-Work (PoW) and Proof-of-Stake (PoS) inspired concepts with real-time network monitoring to secure transactions and maintain blockchain integrity.

# Features

Custom blockchain implementation supporting:
  Proof-of-Work mining: finding a valid hash to add a block
  Proof-of-Stake-inspired logic: balances and pending transactions help determine block acceptance and validity
  
Digital signatures with Elliptic Curve Cryptography (ECC)

Automated detection & mitigation of double-spending attacks:
  Observes pending transactions
  Detects if total spending exceeds balance
  Removes offending transactions and updates the blockchain

Dynamic key and wallet generation

Clear console logs tracing mining, balances and attack prevention

# How It Works

1. Transactions are signed using private keys to ensure authenticity.
2. Mining uses Proof-of-Work: miners solve computational puzzles to add blocks.
3. Balances and pending transactions simulate Proof-of-Stake influence:
     Large senders can be flagged if total outgoing payments exceed their balance.
4. NetworkObserver continuously watches the transaction pool.
5. On detecting suspicious behavior, PeerAlert:
     Removes malicious transactions
     Logs an alert
     Updates blockchain consistency

# Technologies Used

Node.js

crypto-js – hashing with SHA-256

elliptic – ECC for signing & verification (Secp256k1 curve)

# Getting Started

Clone the repository  
  <git clone https://github.com/saumya-singh-14/BlockShield.git  
  cd BlockShield

Install dependencies  
  npm install crypto-js elliptic

Run the project  
  node main.js

# Generate a New Wallet
  
  Create a new wallet key pair anytime:  
    node keygenerator.js  
  This will print a private and public key pair to use for transactions.
