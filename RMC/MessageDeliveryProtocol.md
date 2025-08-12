# MessageDeliveryProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [DeliverMessage](#1-delivermessage) |
| 2 | [DeliverMessageToMultiplePlayers](#2-delivermessagetomultipleplayers) |

# (1) DeliverMessage

## Request

| Type | Name |
|------|------|
| any<Data,string> | oUserMessage |

## Response
This method does not return anything.

# (2) DeliverMessageToMultiplePlayers

## Request

| Type | Name |
|------|------|
| any<Data,string> | oUserMessage |
| std_list<uint32> | lstPrincipals |

## Response
This method does not return anything.

# Types

## TextMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `UserMessage`.

| Type | Name |
|------|------|
| string | m_strTextBody |
