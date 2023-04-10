# crypto_blockchain_

This is a simple implementation of a Proof of Stake (PoS) blockchain using the Flask web framework in Python. The blockchain implementation is represented by the Blockchain class, which maintains a chain of blocks, manages transactions, and supports node registration and conflict resolution. The Flask application provides HTTP endpoints to interact with the blockchain, such as mining a new block and retrieving the entire chain.

Here's a brief overview of the key components in the code:

Blockchain class: This class is responsible for managing the chain of blocks, transactions, and nodes in the network. It has methods for creating new blocks, adding transactions, registering nodes, and resolving conflicts, among others.

Proof of Stake (PoS): Unlike Proof of Work, which requires miners to solve a computationally intensive problem, Proof of Stake selects the node that will mine the next block based on its stake in the network. In this implementation, a simple round-robin selection is used to determine the delegate for each block.

Flask application: The Flask app exposes the following HTTP endpoints:

/mine: Mines a new block and adds it to the blockchain.
/chain: Returns the entire chain of blocks in the blockchain.
Node registration: The register_node method allows nodes to join the network, and the resolve_conflicts method is responsible for ensuring that the nodes have a consistent view of the blockchain.


pip install Flask
To run the application, save the code to a file called blockchain.py and then execute the following command in the terminal:


python crypto.py
This will start the Flask application on your local machine, listening on port 5000. You can then interact with the API using tools like curl or Postman, or by simply accessing the endpoints through your web browser.



To Test:
Crypto.postman_collection.json AND tool like Postman to POST and GET

Create new transactions
Use: http://localhost:5000/transactions/new
<pre>
```json
{
    "message": "Transaction will be added to Block 2"
}
'''
</pre>
To Mine new blocks:
Use: http://localhost:5000/mine

<pre>
```json
{
    "delegate": null,
    "index": 18,
    "message": "New Block Forged",
    "previous_hash": "d796ae3ac8c39e38585a00220b6135b542051116226d08401820a90b4fc0c485",
    "proof": null,
    "transactions": [
        {
            "amount": 1,
            "recipient": "ddf92e41b55f42b3b7c45055cd1c652b",
            "sender": "0"
        }
    ]
}
</pre>
```json

To view the entire blockchain:
Use: http://localhost:5000/chain


<pre>
```json
{
    "chain": [
        {
            "delegate": "0",
            "index": 1,
            "previous_hash": "1",
            "proof": 100,
            "timestamp": 1681145193.8466535,
            "transactions": []
        },
        {
            "delegate": null,
            "index": 2,
            "previous_hash": "442edffa4a74bdd2ebc7ccdb5f3f33c533a84c268bc8959523f1b119b20c83d4",
            "proof": null,
            "timestamp": 1681145198.819354,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "8619e2330a4c477f804bdd10693bbd77",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 3,
            "previous_hash": "11eff089ca68674fe1b054d82a031133e1ccb47525eb6a0ddba3ad640b91795f",
            "proof": null,
            "timestamp": 1681146035.6328635,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "e17f089d76ee4781b87336302b5bd0a4",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 4,
            "previous_hash": "3e78c903a08ea89d6e51d8186b8ae9bcf8ca8fdc07d99b786dcaa8f4fb9a3fc0",
            "proof": null,
            "timestamp": 1681146036.730656,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "a93f45bc81314768b7c61345807a1743",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 5,
            "previous_hash": "0f4ca88f149a658361bfe4a371c34d8f4c885b2274865693b89670293f22af05",
            "proof": null,
            "timestamp": 1681146037.7270312,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "caffac5569324cb98f520b8f831bf439",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 6,
            "previous_hash": "ba45ffa50ecfc7d5e2a443fa4410d6d2f4d41705247f591a13198270e90424b1",
            "proof": null,
            "timestamp": 1681146038.6056817,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "54e936f73f42438da3ced7eb188be9cf",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 7,
            "previous_hash": "be8fd37fd614797c29d346b741a3aae48c3ef64e08c83b109a881b2ea29c496c",
            "proof": null,
            "timestamp": 1681146039.5202663,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "574c8530ffb848588f15d0bbbb6bf6d5",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 8,
            "previous_hash": "5b416c982f08d5db8fbe29da59d5f4da5b4cc1835e3a1bf011b203fe0073a8d2",
            "proof": null,
            "timestamp": 1681146040.4926968,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "4dd3744a276546f085d8f36fcdd2e2fd",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 9,
            "previous_hash": "abc364c8a7442469ab8423f5f1980ef664057881002c6ded683be395cfb8bff7",
            "proof": null,
            "timestamp": 1681146041.7730358,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "f6537947c0054802825fd043c42be982",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 10,
            "previous_hash": "f252e11e5b892a638cb7797f0b630959c5969c7e85cc627450b2937a0d9f07b0",
            "proof": null,
            "timestamp": 1681146042.9768174,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "f18db1fc444c47f78a3f3aa532625789",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 11,
            "previous_hash": "205ff79a2efae529adb82acc681edcf2f67f8dba803556ceb75bfed9a44cc856",
            "proof": null,
            "timestamp": 1681146044.0850747,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "0b3fb47f7c00485c80dac340872e7e88",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 12,
            "previous_hash": "02184a39158bb7a9564b57ad379f54d7c8d4992aaff836ddd0d07f127f9ef239",
            "proof": null,
            "timestamp": 1681146045.0724342,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "fd72a875485447d19f9b599f49bb3f73",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 13,
            "previous_hash": "482978d271564e81bdd0cb5898875324212f95d3e2d1bdf4d2f148baf964e2bf",
            "proof": null,
            "timestamp": 1681146668.6363828,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "42cff7b577e541e38b3a636a0e492fa9",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 14,
            "previous_hash": "24693b589bd9c0dfc3bdd97eb3f12643661241ea0dbcdfe4f0339fded8920c4e",
            "proof": null,
            "timestamp": 1681163457.7740016,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "76f7d62d97d64f1395847ec1b526cc45",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 15,
            "previous_hash": "dc7ac2b8e1d3aea26814db3bbcb9d53c0c1e00b14c7605696765e5a725fa4b5d",
            "proof": null,
            "timestamp": 1681163458.6855633,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "e354fb87bb6d4871a36c67fd7e8841a3",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 16,
            "previous_hash": "c76ac9a1ba6eb52836a36b6b539deb7cb9660d3cf4b9169a2b8afbf943514a91",
            "proof": null,
            "timestamp": 1681163459.6051056,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "80b8a943db934e8fa60805f51ee0023e",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 17,
            "previous_hash": "6b43d5a529bb363ec78c70682ccf531b1ab816d733e0058c13d49a11dc816a0d",
            "proof": null,
            "timestamp": 1681163460.8308263,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "c207415b32244a779dc044a6275a2e63",
                    "sender": "0"
                }
            ]
        },
        {
            "delegate": null,
            "index": 18,
            "previous_hash": "d796ae3ac8c39e38585a00220b6135b542051116226d08401820a90b4fc0c485",
            "proof": null,
            "timestamp": 1681163461.7782924,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "ddf92e41b55f42b3b7c45055cd1c652b",
                    "sender": "0"
                }
            ]
        }
    ],
    "length": 18
</pre>
```json
