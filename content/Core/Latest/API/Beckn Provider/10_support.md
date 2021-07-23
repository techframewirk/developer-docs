---
title: "Support"
metaTitle: "Beckn for Developers"
metaDescription: "Documentation for developers of the Beckn ecosystem"
---

Support
===================

>   Contact support

Overview
--------

>   The BAP will send the id of an entity for which support is required from the BPP.

Request
-------

### URL

>   /support

### Method

>  *POST*

### Request Body Schema

|**Field**|**Type**|
|---------|--------|
|context*|[ContextForSupport](/Core/Latest/02_Schemas/contextforsupport)|
|message| [MessageForSupport](/Core/Latest/02_Schemas/messageforsupport) |

### Request Body Example

```
{
    "context": {
        "domain": "nic2004:52110",
        "country": "IND",
        "city": "std:080",
        "action": "support",
        "core_version": "0.9.1",
        "bap_id": "https://mock_bap.com/",
        "bap_uri": "https://mock_bap.com/beckn/",
        "bpp_id": "https://mock_bpp.com/",
        "bpp_uri": "https://mock_bpp.com/beckn/",
        "transaction_id": "1209849124",
        "message_id": "12341242321",
        "timestamp": "2021-03-23T10:00:40.065Z"
    },
    "message": {
        "ref_id": "order_1"
    }
}
```

>   Here the BAP is requesting support for *order_1* to the BPP.

Response
--------

### Response Body Schema

|**Field**|**Type**|
|---------|--------|
|message*|{ [Ack](/Core/Latest/02_Schemas/ack) }|
|error| [Error](/Core/Latest/02_Schemas/error) |

### Response Body Example

```
{
  "message": {
    "ack": {
      "status": "ACK"
    }
  }
}
```

> Acknowldegement response

### Response Codes

| **Code**       | **Description** |
|----------------|-----------------|
| 200 | Acknowledgement of message received   |