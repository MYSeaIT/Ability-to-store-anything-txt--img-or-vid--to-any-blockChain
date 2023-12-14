# IPFS File Storage and Blockchain Interaction

This Node.js application demonstrates secure file storage on IPFS and recording file hashes onto the Ethereum blockchain using a provided smart contract. The app utilizes various libraries such as `fs`, `ipfs-http-client`, and `web3` for file handling, IPFS interaction, and blockchain integration.

## Setup

1. **Clone Repository:** Clone the repository locally using `git clone [repository_url]`.
2. **Install Dependencies:** Run `npm install` or `yarn install` to install required dependencies.
3. **Configuration:** Set environment variables or create a config file for IPFS host, port, protocol, blockchain node URL, smart contract address, etc.

## Usage

- Replace `exampleFilePath` and `fromAddress` variables in the code with actual file path and Ethereum address.
- Run the main script: `node main.js [file_path] [ethereum_address]`.
  - Replace `[file_path]` and `[ethereum_address]` with your file path and Ethereum address, respectively.

### Code Explanation

- The app initializes IPFS and connects to a blockchain node using provided configurations.
- `storeToIPFSWithEvents(filename)`: Reads a file from the local system and uploads it to IPFS, emitting events for different stages.
- `storeHashOnBlockchainWithContract(hash, fromAddress)`: Interacts with an Ethereum smart contract to store the IPFS hash on the blockchain.
- Error handling: Validations for input and error event emission with appropriate error messages.

### Error Handling

- **Input Validation:** Checks for null or undefined input, throwing an error if validation fails.
- **Error Events:** Emits 'error' events with error messages for any encountered errors during file handling, IPFS or blockchain interactions.

## Additional Notes

- Ensure an Ethereum node is running locally or provide the appropriate blockchain node URL.
- The smart contract ABI and address must be correctly provided for interaction with the deployed smart contract.

## Contribution

Contributions, bug reports, and suggestions are welcome. Feel free to open an issue or a pull request.

## Disclaimer

This is a demonstration application; exercise caution with real data and blockchain transactions.
