# UbiFriendsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RequestFriendship](#1-requestfriendship) |
| 2 | [AcceptFriendship](#2-acceptfriendship) |
| 3 | [ClearRelationship](#3-clearrelationship) |
| 4 | [DeclineFriendship](#4-declinefriendship) |
| 5 | [AddToBlacklist](#5-addtoblacklist) |
| 6 | [RemoveFromBlacklist](#6-removefromblacklist) |
| 7 | [GetRelationshipsList](#7-getrelationshipslist) |

# (1) RequestFriendship

## Request

| Type | Name |
|------|------|
| AccountInfo | to |

## Response
This method does not return anything.

# (2) AcceptFriendship

## Request

| Type | Name |
|------|------|
| AccountInfo | to |

## Response
This method does not return anything.

# (3) ClearRelationship

## Request

| Type | Name |
|------|------|
| AccountInfo | to |

## Response
This method does not return anything.

# (4) DeclineFriendship

## Request

| Type | Name |
|------|------|
| AccountInfo | to |

## Response
This method does not return anything.

# (5) AddToBlacklist

## Request

| Type | Name |
|------|------|
| AccountInfo | to |

## Response
This method does not return anything.

# (6) RemoveFromBlacklist

## Request

| Type | Name |
|------|------|
| AccountInfo | to |

## Response
This method does not return anything.

# (7) GetRelationshipsList

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| qlist<RelationshipInfo> | relationshipsList |

# Types

## AccountInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_principalId |
| string | m_ubiAccountId |

## RelationshipInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| AccountInfo | m_from |
| AccountInfo | m_to |
| byte | m_relationship |
| bool | m_onBlacklist |
| datetime | m_friendsDate |
