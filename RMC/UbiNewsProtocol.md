# UbiNewsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetChannel](#1-getchannel) |
| 2 | [GetNewsHeaders](#2-getnewsheaders) |
| 3 | [GetNewsMessages](#3-getnewsmessages) |

# (1) GetChannel

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [NewsChannel](#newschannel-structure) | newsChannel |

# (2) GetNewsHeaders

## Request

| Type | Name |
|------|------|
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| qlist<[NewsHeader](#newsheader-structure)> | newsHeaders |

# (3) GetNewsMessages

## Request

| Type | Name |
|------|------|
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| qlist<[NewsMessage](#newsmessage-structure)> | newsMessages |

# Types

## NewsChannel ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_ownerPID |
| string | m_name |
| string | m_description |
| datetime | m_creationTime |
| datetime | m_expirationTime |
| string | m_type |
| string | m_locale |
| bool | m_subscribable |

## NewsHeader ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_recipientID |
| uint32 | m_recipientType |
| uint32 | m_publisherPID |
| string | m_publisherName |
| datetime | m_publicationTime |
| datetime | m_displayTime |
| datetime | m_expirationTime |
| string | m_title |
| string | m_link |

## NewsMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `NewsHeader`.

| Type | Name |
|------|------|
| string | m_body |
