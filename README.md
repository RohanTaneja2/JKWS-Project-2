# JWKS Server with SQLite Backed Storage

This project extends a basic JWKS (JSON Web Key Set) server to incorporate SQLite-backed storage for private keys. It enhances security by storing keys in a persistent database, ensuring availability even after server restarts.

## Table of Contents

- [Background](#background)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Testing](#testing)

## Background

In the realm of cybersecurity, ensuring secure authentication processes is crucial. This project addresses the need for fortifying authentication systems against threats like SQL injection by utilizing a database to store private keys securely.

## Requirements

- Python 3.x
- SQLite
- Additional Python packages (see [requirements.txt](requirements.txt))

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/jwks-server.git
cd jwks-server
```
Install dependencies:
```bash

pip install -r requirements.txt
```
Create the SQLite database file:
```bash

sqlite3 totally_not_my_privateKeys.db < private_keys_schema.sql
```
## Usage
Start the server:
```bash
python jwks_server.py
```
The server will be accessible at http://localhost:8080.
## Endpoints
POST /auth: Generates and returns a JWT token.
GET /.well-known/jwks.json: Retrieves public keys in JWKS format.

## Testing
Ensure the server is running.

Run the provided test client:

```bash
python test_client.py
```
