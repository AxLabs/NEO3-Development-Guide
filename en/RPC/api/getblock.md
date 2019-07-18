﻿# getblock Method

The corresponding block information is returned according to the specified hash value.

## Parameter Description

Hash: Block hash value.

Verbose: Optional, the default value of verbose is 0. When verbose is 0, the serialized information of the block is returned, represented by a hexadecimal string. If you need to get detailed information, you will need to use the SDK for deserialization. When verbose is 1, detailed information of the corresponding block in Json format string, is returned.

## Example

Request body:

```json
{
  "jsonrpc": "2.0",
  "method": "getblock",
  "params": ["479d71eae26a817647a373381f21de06c5e4bf3ee7717c948f006ce8e25441be"],
  "id": 1
}
```

Response body:

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0000000000000000000000000000000000000000000000000000000000000000000000008e29af06ec157a3d85717b1eb7317c3ef4049a7222d76c6dd4d5a24598c6571665fc885700000000f071d5fc6d2e2978a45842f05b1ac970e87d197700015102001dac2b7c0000000000000000000568123e7fe8da1745e9b549bd0bfa1a569971c77eba30cd5a4b000000000000000000000000000000000000000000000151"
}
```

Request body:

verbose = 1，返回 JSON 格式的结果。

```json
{
  "jsonrpc": "2.0",
  "method": "getblock",
  "params": ["479d71eae26a817647a373381f21de06c5e4bf3ee7717c948f006ce8e25441be", 1],
  "id": 1
}
```

Response body:

```json
{
    "jsonrpc": "2.0", 
    "id": "1", 
    "result": {
        "hash": "0x479d71eae26a817647a373381f21de06c5e4bf3ee7717c948f006ce8e25441be", 
        "size": 164, 
        "version": 0, 
        "previousblockhash": "0x0000000000000000000000000000000000000000000000000000000000000000", 
        "merkleroot": "0x1657c69845a2d5d46d6cd722729a04f43e7c31b71e7b71853d7a15ec06af298e", 
        "time": 1468595301, 
        "index": 0, 
        "nextconsensus": "AdhEBzaBZujuj5kEiwvKmMVy5ydqj3AC3V", 
        "witness": {
            "invocation": "", 
            "verification": "51"
        }, 
        "consensus_data": {
            "primary": 0, 
            "nonce": "000000007c2bac1d"
        }, 
        "tx": [
            {
                "txid": "0xdd4372964d52e800e07b7d1c536a0ad29022edbf506603c01a4efa6cc0b4e1c6", 
                "size": 55, 
                "version": 0, 
                "nonce": 0, 
                "script": "68123e7fe8", 
                "sender": "Abf2qMs1pzQb8kYk9RuxtUb9jtRKJVuBJt", 
                "gas": "0", 
                "net_fee": "0", 
                "valid_until_block": 0, 
                "attributes": [ ], 
                "witness": {
                    "invocation": "", 
                    "verification": "51"
                }
            }
        ], 
        "confirmations": 6180, 
        "nextblockhash": "0x1c00023b24ba5328918f4a0adc35607c8f97913fdda88b4eb4c571e7bc613bf4"
    }
}
```
