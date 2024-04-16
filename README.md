# Ether Private Bank API

Welcome to the Ether Private Bank API repository. This NestJS-based backend serves as a bridge between traditional finance and blockchain technology, offering a secure entry point to decentralized finance (DeFi) investments. Our system supports asset tokenization, facilitates Elion transactions, and integrates with DeFi protocols via Chainlink and ethers.js.

## API Version

Version: 1.0.0

## API Endpoints Overview

This API provides various services through multiple endpoints categorized by their functionality. Below is a high-level overview of the available endpoints and their purposes:

### Health Checks
- `GET /health/status` - Returns the health status of the backend.

### Wallet Services
- `POST /wallets/get-or-create-hsm-wallet` - Retrieves or creates an HSM wallet address.
- `POST /wallets/create-hsm-key` - Creates a new HSM key.
- `GET /wallets/public-key-info/{keyName}` - Fetches public key information.
- `POST /wallets/transactions/sign` - Signs a transaction.
- `POST /wallets/transactions/prepare` - Prepares a transaction.
- `GET /wallets/hsm-wallet-address/{keyName}` - Retrieves an HSM wallet address.
- `DELETE /wallets/delete-hsm-key/{keyName}` - Deletes an HSM key.
- `GET /wallets/{walletId}/tokens/{contractAddress}/balance` - Fetches ERC20 token balance.
- `POST /wallets/roles` - Grants roles to addresses.

### Payment Services
- `GET /payments` - Lists all payments.
- `GET /payments/subaccount/{supabaseId}` - Lists transactions by supabase ID.
- `POST /payments/account/{accountId}` - Creates a payment link.
- `POST /payments/process-webhook` - Processes a payment webhook.
- `POST /payments/buyers` - Creates a new buyer.

### Boletos Services
- `POST /boletos` - Creates multiple boletos.
- `GET /boletos` - Lists all boletos.
- `POST /boletos/subaccount/{supabaseId}` - Creates boletos for a specified subaccount.
- `GET /boletos/{id}` - Retrieves a specific boleto.
- `DELETE /boletos/{id}` - Deletes a specific boleto.
- `GET /boletos/{id}/pdf` - Retrieves a PDF version of a boleto.
- `POST /boletos/webhook` - Handles boleto payment webhook.
- `POST /boletos/pay` - Pays a boleto.

### BRCode Services
- `POST /brcodes` - Creates dynamic BRCodes.
- `GET /brcodes` - Lists all dynamic BRCodes.
- `POST /brcodes/subaccount/{supabaseId}` - Creates dynamic BRCodes for a specified subaccount.
- `GET /brcodes/{id}` - Retrieves a specific dynamic BRCode.
- `POST /brcodes/webhook` - Handles Pix payment webhook.
- `POST /brcodes/pay` - Makes a BRCode payment.

### Banking Services
- `GET /banking/balance` - Retrieves balance information.
- `GET /banking/transactions` - Lists all transactions.
- `GET /banking/transaction/{id}` - Retrieves a specific transaction by ID.

## Authentication

This API uses JWT for authentication. Ensure that your requests include a valid `Authorization` header with a bearer token to access the endpoints.

## Contributions

Contributions to this project are welcome. Please fork the repository and submit a pull request for review.
