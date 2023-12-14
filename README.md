# SubQuery - Example Project for Autonity Piccadilly

# DEMO:
https://autonity-subql-demo-ntn.web3cdn.services/


This project Wrapped NTN Token.
0xBd770416a3345F91E4B34576cb804a576fa48EB1

## Query your project

For this project, you can try to query with the following GraphQL code to get a taste of how it works.

```graphql
{
  query {
    transfers(first: 5, orderBy: VALUE_DESC) {
      totalCount
      nodes {
        id
        blockHeight
        from
        to
        value
        contractAddress
      }
    }
  }
  approvals(first: 5, orderBy: BLOCK_HEIGHT_DESC) {
    nodes {
      id
      blockHeight
      owner
      spender
      value
      contractAddress
    }
  }
}
```

The result should look something like this:

```json
{
  "data": {
    "query": {
      "transfers": {
        "totalCount": 7,
        "nodes": [
          {
            "id": "0xfc02d66a2d170df9fb307fc48480a4acb748b0c5cd3e5c06056b701f25bf73d4",
            "blockHeight": "29607355",
            "from": "0x30628e843Bd9A10fc475aa3baA9fF1D08333960a",
            "to": "0xc9Be70c32693970172F2b7d3C828673314086e7b",
            "value": "47400212415827049",
            "contractAddress": "0xA6FA4fB5f76172d178d61B04b0ecd319C5d1C0aa"
          },
          {
            "id": "0x5e676271eeca2f20cde3e09334b75037bbc8a58f667832462bae3b902b9fc377",
            "blockHeight": "29605828",
            "from": "0x2d975bDa61d89d35f259dAdeAe40693fA17842B8",
            "to": "0xEB8385A83fd9D91889c60487Aeb2F4495F04c9F9",
            "value": "10144216690787271",
            "contractAddress": "0xA6FA4fB5f76172d178d61B04b0ecd319C5d1C0aa"
          },
          {
            "id": "0x43cdf37475fde8e5620b6f732f0550a4c7dab67a7a61f460b60c9c51a3e57e9f",
            "blockHeight": "29606975",
            "from": "0xc1FF5D622aEBABd51409e01dF4461936b0Eb4E43",
            "to": "0x39f3b9C8585Fc57A57EC39322E92Face43484D97",
            "value": "136565991130049",
            "contractAddress": "0xA6FA4fB5f76172d178d61B04b0ecd319C5d1C0aa"
          },
          {
            "id": "0x1fe11447c36069cd93bf446e4a3093513ed5893d6326dcaac8bac283ab559bca",
            "blockHeight": "29607247",
            "from": "0x39f3b9C8585Fc57A57EC39322E92Face43484D97",
            "to": "0xcDe7a88a1dada60CD5c888386Cc5C258D85941Dd",
            "value": "96250000000000",
            "contractAddress": "0xA6FA4fB5f76172d178d61B04b0ecd319C5d1C0aa"
          },
          {
            "id": "0x3857be80c2478f56ea5bdece0993658b951c24cb8028f2b52c2547d4787bec33",
            "blockHeight": "29607290",
            "from": "0xcDe7a88a1dada60CD5c888386Cc5C258D85941Dd",
            "to": "0x39f3b9C8585Fc57A57EC39322E92Face43484D97",
            "value": "87500000000000",
            "contractAddress": "0xA6FA4fB5f76172d178d61B04b0ecd319C5d1C0aa"
          }
        ]
      }
    },
    "approvals": {
      "nodes": [
        {
          "id": "0xa4ca08a96a8ffbf66141a70c20c8e9685c5c620779d5b019408df4f65b1aa315",
          "blockHeight": null,
          "owner": "0x39f3b9C8585Fc57A57EC39322E92Face43484D97",
          "spender": "0x1E0049783F008A0085193E00003D00cd54003c71",
          "value": "115792089237316195423570985008687907853269984665640564039457584007913129639935",
          "contractAddress": "0xA6FA4fB5f76172d178d61B04b0ecd319C5d1C0aa"
        }
      ]
    }
  }
}
```
