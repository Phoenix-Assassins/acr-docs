# ContactsExtensionsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RetrieveContactSessionPS3](#1-retrievecontactsessionps3) |
| 2 | [RetrieveContactsSessionListPS3](2-retrievecontactssessionlistps3) |

# (1) RetrieveContactSessionPS3

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | contactName |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure)> | sessions |

# (2) RetrieveContactsSessionListPS3

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | contactNames |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure)> | sessions |

# Types

## GameSessionByPlayerInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString |
| Uint32 | unkUint |
| Bool | unkBool1 |
| Bool | unkBool2 |
| [GameSessionSearchResult](https://github.com/kinnay/NintendoClients/wiki/Game-Session-Protocol#gamesessionsearchresult-structure) | gameSesSearchResult |
