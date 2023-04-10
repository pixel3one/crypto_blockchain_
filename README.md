# crypto_blockchain_

This is a simple implementation of a blockchain in Python using the Flask web framework. The Blockchain class defines the structure and methods for creating and managing the blockchain. It contains methods for registering nodes, validating chains, resolving conflicts, creating new blocks and transactions, and performing proof of stake for block creation.

The Flask web application exposes the following endpoints:

/mine: This endpoint mines a new block on the blockchain. It retrieves the last block, gets the proof of stake value, and creates a new transaction with a mining reward. Then, it creates a new block with the proof of stake value and the hash of the last block, and returns a JSON object with the new block's details.

/chain: This endpoint returns the full chain of the blockchain as a JSON object, along with its length.

To run this application, you will need to have Flask and the necessary dependencies installed. You can install Flask using pip:


pip install Flask
To run the application, save the code to a file called blockchain.py and then execute the following command in the terminal:


python crypto.py
This will start the Flask application on your local machine, listening on port 5000. You can then interact with the API using tools like curl or Postman, or by simply accessing the endpoints through your web browser.



To Test:
Crypto.postman_collection.json AND tool like Postman to POST and GET

Create new transactions
Use: http://localhost:5000/transactions/new

To Mine new blocks:
Use: http://localhost:5000/mine

To view the entire blockchain:
Use: http://localhost:5000/chain
