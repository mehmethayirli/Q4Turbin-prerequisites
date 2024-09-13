# Turbin3 Q4 Airdrop Project

TX Link: https://explorer.solana.com/tx/2XvV2QXMLA1zm5RfR4E145KpnrUhfCj1SzjM43txFyc3gB8nfEHGLJWPXpzhdzCZ1cswwPS8eYWNjLep4tingqZy?cluster=devnet](https://explorer.solana.com/tx/oyKjF2egedzYpa5p4pjG13iTQjVcZnG7mQMWbJxL45G6sNscVPHVdb71i56D5VyUzKSuseDRhDqK4iRbwAoybRA?cluster=devnet

---

**wb_prereq**: This script configures how a program interacts with the Solana blockchain. The `WbaPrereq` type outlines the version, name, and program address. The script contains instructions like `complete` and `update`, which specify the necessary accounts and arguments. It also includes the account structure `Q2Prereq2024`, the error code `InvalidGithubAccount`, and relevant data types. The IDL provides the structure and details for interacting with the program.

_Run the script with the command:_ `yarn wba_prereq`

---

**airdrop.ts**: This script facilitates transferring 2 SOL to a specified wallet on the Solana blockchain. It imports the `Connection`, `Keypair`, and `LAMPORTS_PER_SOL` modules. The private key for the wallet is retrieved from the `wallet` JSON file, and a `Keypair` is generated. A `Connection` object connects to the Solana devnet, and within an asynchronous function, the `requestAirdrop` method is called to send 2 SOL to the wallet. If successful, the transaction hash is displayed; if not, an error message is shown.

_Run the script with the command:_ `yarn airdrop`

---

**enroll.ts**: This script sends a `complete` instruction to a Solana blockchain program. It imports the `Connection`, `Keypair`, and `PublicKey` modules from `@solana/web3.js`, and the `Program`, `Wallet`, and `AnchorProvider` modules from `@coral-xyz/anchor`. The program's IDL and `WbaPrereq` are imported to reference the program structure. The private key is retrieved from the `wallet` JSON, and a `Keypair` is generated. The connection and wallet are set using `AnchorProvider`. The program account is located using `findProgramAddressSync`, and the `complete` instruction is sent with the Github data in an asynchronous function. A successful transaction returns a hash; otherwise, an error message is logged.

_Run the script with the command:_ `yarn enroll`

---

**keygen.ts**: This script generates a new Solana wallet and prints its details. It imports the `Keypair` module from `@solana/web3.js` and creates a new wallet with `Keypair.generate()`. The public and secret keys of the wallet are printed to the console, with the public key displayed using `publicKey.toBase58()` and the secret key shown as a byte array.

_Run the script with the command:_ `yarn keygen`

---

**transfer.ts**: This script handles transferring SOL between two wallets on the Solana blockchain. It imports modules such as `Transaction`, `SystemProgram`, `Connection`, `Keypair`, `LAMPORTS_PER_SOL`, `sendAndConfirmTransaction`, and `PublicKey` from `@solana/web3.js`. The private key is loaded from the `wallet` JSON file to create a `Keypair`, and a second wallet's public key is specified. A connection to the devnet is established, and a transaction for transferring SOL is created using `SystemProgram.transfer` within an asynchronous function. The transaction is signed, sent, and confirmed. Upon success, the transaction hash is returned; otherwise, an error message is printed.

_Run the script with the command:_ `yarn transfer`

---

**dev-wallet.json, dev-wallet2.json, dev-wallet3.json**: These JSON files contain byte arrays representing the secret keys for Solana wallets. In Solana, secret keys in this format are used to generate a wallet `Keypair`.

---

**package.json**: Defines project metadata, scripts, and lists the necessary dependencies for the project.

---

**package-lock.json**: Ensures consistent installation of dependencies by locking the exact versions and structure.

---

**yarn.lock**: Locks the precise versions of all dependencies and sub-dependencies to guarantee consistent project behavior across different environments.

---
