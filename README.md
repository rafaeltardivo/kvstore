# KVStore

A simple key-value store with HTTP API and transaction logging.

## Recent Updates

- Removed duplicate global variables and functions to avoid redeclaration errors.
- Fixed method redeclaration in `FileTransactionLogger`.
- Improved error handling in HTTP handlers to avoid potential panics.
- Enhanced concurrency safety with proper mutex usage.

## Features

- HTTP API for key-value operations.
- Transaction logging for data persistence.
- Concurrent access support with mutex protection.

## Usage

Run the service:
```bash
go run .
```

The service will start on `:8080` and expose the following endpoints:
- `PUT /v1/{key}` - Store a value for a key.
- `GET /v1/{key}` - Retrieve a value for a key.
