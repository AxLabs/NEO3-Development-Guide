﻿# dumpprivkey Method

Exports the private key of the specified address.

> You should call the `openwallet` method to open the wallet first.



```json
{
  "jsonrpc": "2.0",
  "method": "dumpprivkey",
  "params": [address]
  "id": 1
}
```



### Parameter Description

* address：To export the addresses of the private key, the address is required as a standard address.



## Example

Request body:

```json
{
  "jsonrpc": "2.0",
  "method": "dumpprivkey",
  "params": ["ASMGHQPzZqxFB2yKmzvfv82jtKVnjhp1ES"],
  "id": 1
}
```

Response body:

```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": "L3FdgAisCmV******************************9XM65cvjYQ1"
}
```

Response Description:

Returns the private key of the standard address.