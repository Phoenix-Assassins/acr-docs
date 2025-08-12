# GameSessionAdminProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetTableStatuses](#1-gettablestatuses) |
| 2 | [ForceCustomTableSync](#2-forcecustomtablesync) |
| 3 | [CleanupOnBootSessions](#3-cleanuponbootsessions) |
| 4 | [CleanupOnBootURLs](#4-cleanuponbooturls) |
| 5 | [GetURLs](#5-geturls) |
| 6 | [UpdateURLsDID](#6-updateurlsdid) |
| 7 | [SetThrottlingProbability](#7-setthrottlingprobability) |
| 8 | [SetThrottlingDelay](#8-setthrottlingdelay) |
| 9 | [GetSession](#9-getsession) |

# (1) GetTableStatuses

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| qlist<GameSessionTableStatus> | gameSessionTableStatuses |

# (2) ForceCustomTableSync

## Request

| Type | Name |
|------|------|
| qlist<GameSessionTableDetail> | gameSessionTableDetails |

## Response
This method does not return anything.

# (3) CleanupOnBootSessions

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| uint32 | nbOfAffectedRows |

# (4) CleanupOnBootURLs

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| uint32 | nbOfAffectedRows |

# (5) GetURLs

## Request

| Type | Name |
|------|------|
| uint32 | pid |

## Response

| Type | Name |
|------|------|
| qlist<stationurl> | urls |

# (6) UpdateURLsDID

## Request

| Type | Name |
|------|------|
| uint32 | pid |
| uint32 | did |

## Response
This method does not return anything.

# (7) SetThrottlingProbability

## Request

| Type | Name |
|------|------|
| uint32 | typeID |
| uint32 | throttlingPercentage |

## Response
This method does not return anything.

# (8) SetThrottlingDelay

## Request

| Type | Name |
|------|------|
| uint32 | typeID |
| uint32 | throttlingDelaySeconds |

## Response
This method does not return anything.

# (9) GetSession

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response

| Type | Name |
|------|------|
| GameSessionSearchResult | searchResult |

# Types

## GameSessionTableStatus ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_tableName |
| string | m_engine |
| datetime | m_creationTime |

## GameSessionTableDetail ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_tableName |
| string | m_generatorVersion |
| string | m_xmlHash |
