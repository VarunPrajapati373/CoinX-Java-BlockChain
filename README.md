# CoinX - A Simple Cryptocurrency

CoinX is a basic implementation of a cryptocurrency using Java. This project is to help understand the fundamentals of blockchain, cryptographic signatures, transactions, and wallets.

## Features

- **Blockchain**: A simple, verifiable blockchain that stores transactions.
- **Wallets**: Generates Elliptic Curve KeyPairs for public and private keys. The public key serves as the address, while the private key is used for signing transactions.
- **Transactions**: Includes inputs and outputs, enabling the transfer of CoinXs between wallets. Transactions are signed and verified using cryptographic signatures.
- **Merkle Root**: Used for efficient transaction verification within blocks.
- **Genesis Block**: The first block that initializes the blockchain and releases CoinXs to a specified wallet.

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or higher.
- Maven (for managing dependencies).
- BouncyCastle library (for cryptographic operations).
- GSON library (for JSON parsing).

### Installing Dependencies

1. **BouncyCastle**: 

    Add the following to your `pom.xml` to include the BouncyCastle library:

    ```xml
    <dependency>
        <groupId>org.bouncycastle</groupId>
        <artifactId>bcprov-jdk15on</artifactId>
        <version>1.70</version>
    </dependency>
    ```

2. **GSON**:

    Add the following to your `pom.xml` to include the GSON library:

    ```xml
    <dependency>
        <groupId>com.google.code.gson</groupId>
        <artifactId>gson</artifactId>
        <version>2.8.9</version>
    </dependency>
    ```
    
### Testing the Wallets and Transactions

The main method in the `coinx chain` class demonstrates the following:

- Creating two wallets (`walletA` and `walletB`).
- Generating a transaction from `walletA` to `walletB`.
- Signing and verifying the transaction.
- Adding the transaction to a block and updating the blockchain.

### Understanding the Code

1. **Wallet Class**:

    - Holds public and private keys.
    - Generates and signs transactions.

2. **Transaction Class**:

    - Represents a transaction with inputs, outputs, and a cryptographic signature.
    - Includes methods to generate and verify the signature.

3. **TransactionInput and TransactionOutput Classes**:

    - `TransactionInput`: References to previous transaction outputs (UTXOs).
    - `TransactionOutput`: Shows the amount sent to each party and is referenced in new transactions.

4. **Block Class**:

    - Represents a block in the blockchain.
    - Contains a list of transactions and the Merkle root of those transactions.

5. **coinx chain Class**:

    - Manages the blockchain.
    - Includes methods to validate the chain and add transactions to blocks.


*Note*: This is a simple educational project and is not meant for real-world use as a cryptocurrency.
