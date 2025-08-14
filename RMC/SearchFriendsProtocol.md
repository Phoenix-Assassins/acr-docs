# SearchFriendsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SearchFriends](#1-searchfriends) |

# (1) SearchFriends
## Request
| Type | Name |
|------|------|
| string | name |

## Response
| Type | Name |
|------|------|
| List<[FriendSearchResult](#friendsearchresult-structure)> | results |

# Types

## FriendSearchResult
| Type | Name |
|------|------|
| uint32 | pid |
| string | name |
