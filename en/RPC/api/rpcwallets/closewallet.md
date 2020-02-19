# closewallet 

Close the wallet.

```json
{
  "jsonrpc": "2.0",
  "method": "closewallet",
  "params": []
  "id": 1
}
```

## Example

Request Body：

```json
{
  "jsonrpc": "2.0",
  "method": "closewallet",
  "params": [],
  "id": 1
}
```

Response Body：

```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": true
}
```

Response Description：

Return whether the wallet was successfully closed or not.