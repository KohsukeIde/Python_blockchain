# Simple blockchain with Python

# blockchain.py
This file implements a simple blockchain data structure in Python.

It contains the following classes:

Block: A class that represents a single block in the blockchain. It contains a block number, a list of transactions, a nonce (a random number used to create a unique hash), and the hash of the previous block.
Blockchain: A class that represents a full blockchain. It contains a list of blocks and has functions for adding new blocks and validating the chain.
# blockchain_server.py
This file implements a RESTful API for interacting with the blockchain. It uses the Flask framework to create endpoints for adding transactions and blocks to the chain.

It has the following routes:

/transactions: A POST endpoint for adding transactions to the blockchain. It expects a JSON payload with the following keys: sender_blockchain_address, recipient_blockchain_address, sender_public_key, value, and signature.
/mine: A GET endpoint for mining new blocks. This involves adding a block to the chain that contains all unconfirmed transactions and a nonce that results in a unique hash.
/chain: A GET endpoint for retrieving the entire blockchain.
# wallet.py
This file implements a simple wallet for cryptocurrency transactions.

It contains the following classes:

Wallet: A class that represents a wallet and contains a private key, a public key, and a blockchain address.
Transaction: A class that represents a transaction between wallets. It contains the sender's private key, public key, and blockchain address, the recipient's blockchain address, and the value being transferred. It also generates a signature using the sender's private key.
# wallet_server.py
This file implements a RESTful API for interacting with the wallet. It uses the Flask framework to create endpoints for creating new wallets and transactions.

It has the following routes:

/wallet: A POST endpoint for creating a new wallet. It returns a JSON payload with the following keys: private_key, public_key, and blockchain_address.
/transaction: A POST endpoint for creating a new transaction. It expects a JSON payload with the following keys: sender_private_key, sender_blockchain_address, recipient_blockchain_address, sender_public_key, and value.
/wallet/amount: A GET endpoint for retrieving the amount of cryptocurrency associated with a wallet's blockchain address. It expects a query parameter of blockchain_address.
